# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.hostmanager.enabled = true
  config.hostmanager.manage_host = true

  config.vm.box = "ubuntu/trusty64"
  config.vm.network :private_network, ip: "192.168.50.10"
  config.vm.hostname = "mesos.local"

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "mesos-install.yml"
  end
end
