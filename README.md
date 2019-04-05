# vagrant-minikube

```
vagrant up
vagrant ssh

export MINIKUBE_WANTUPDATENOTIFICATION=false
export MINIKUBE_WANTREPORTERRORPROMPT=false
export MINIKUBE_HOME=$HOME
export CHANGE_MINIKUBE_NONE_USER=true
mkdir -p $HOME/.kube
touch $HOME/.kube/config

export KUBECONFIG=$HOME/.kube/config
sudo -E /usr/local/bin/minikube start --vm-driver=none --extra-config=kubeadm.ignore-preflight-errors=NumCPU
```

or  
Vagrantfile:

```
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
+   vb.cpus = "2"
  end
```

```
sudo -E /usr/local/bin/minikube start --vm-driver=none
```
