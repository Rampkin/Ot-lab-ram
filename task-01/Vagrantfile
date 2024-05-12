# -*- mode: ruby -*-
# vi: set ft=ruby :
ENV['VAGRANT_SERVER_URL'] = 'https://vagrant.elab.pro'

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/focal64"
  config.vm.box_version = "1.0.0"

  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vm.provider "virtualbox" do |vb|
 
     vb.memory = "1024"
     vb.cpus = "1"
  end

   config.vm.provision "shell", inline: <<-SHELL
     apt-get update
     apt-get install -y apache2
   SHELL
end
