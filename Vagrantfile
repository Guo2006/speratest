# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.provider "virtualbox" do |v|
    v.memory = "1024"
    v.cpus = 2
  end

  config.vm.define "host1" do |host1|
    host1.vm.box = "centos/7"
    host1.vm.network :private_network, ip: "192.168.10.105"
#   config.vm.network :forwarded_port, guest: 22, host: 1234
    host1.vm.network :forwarded_port, guest: 8080, host: 8081
  

    

    host1.vm.provision "ansible" do |ansible|
      ansible.playbook = "provisioning/playbook.yaml"
      ansible.verbose = "vv"
      ansible.inventory_path = ".vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory"
    end
  end     

  config.vm.define "host2" do |host2|
    host2.vm.box = "centos/7"
    host2.vm.network :private_network, ip: "192.168.10.106"


    host2.vm.provision "ansible" do |ansible|
      ansible.playbook = "provisioning/playbook2.yaml"
      ansible.verbose = "vv"
      ansible.inventory_path = ".vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory"
    end
  end

    
end
