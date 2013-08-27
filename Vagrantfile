# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.box = "precise64"
  config.vm.network :private_network, ip: "192.168.111.222"

  Vagrant.configure("2") do |config|
    config.vm.provision :ansible do |ansible|
      ansible.playbook = "laravel.yml"
      ansible.inventory_file = "vagrant_hosts"
    end
  end
end
