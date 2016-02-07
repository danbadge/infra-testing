# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.hostmanager.enabled = true
  config.hostmanager.manage_host = true
  config.hostmanager.ignore_private_ip = false
  config.hostmanager.include_offline = true
  config.vm.define 'mesos.local' do |node|
    node.vm.hostname = 'mesos.local'
    node.vm.network :private_network, ip: '192.168.50.10'
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "mesos-install.yml"
  end
end
