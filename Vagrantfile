Vagrant.configure("2") do |config|
  config.vm.box = "bento/centos-7.5"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
  end
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "ansible/playbook.yml"
    ansible.verbose = "-vvv"
    ansible.inventory_path = "ansible/inventory"
    ansible.extra_vars = {
      hostname: "localhost"
    }
  end
end
