# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.box = "precise32"
  config.vm.network :hostonly, "192.168.33.11"

  config.vm.provision :shell, :inline => "echo \"Europe/London\" | sudo tee /etc/timezone && dpkg-reconfigure --frontend noninteractive tzdata"

  config.vm.forward_port 80, 8080
  config.vm.forward_port 3306,3366
  
  config.vm.share_folder("v-web", "/var/www", "./site", :owner => "www-data", :group => "www-data")
end

Vagrant.configure("2") do |config|
  config.vm.provider :virtualbox do |vb|
      vb.name = "php-dev"
  end
  config.vm.provision :ansible do |ansible|
      ansible.sudo = true
      ansible.verbose = true
      ansible.playbook = "provisioning/laravel.yml"
      ansible.inventory_path = "provisioning/vagrant_hosts"
    end
end
