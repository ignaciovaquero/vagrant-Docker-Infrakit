# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 1024
    vb.cpus = 1
  end
  config.vm.synced_folder "ansible/", "/vagrant"

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "infrakit.yml"
  end
end
