# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  # Box Update
  config.vm.box_check_update = false
  config.vbguest.auto_update = false

  # Port Forwarding
  config.vm.network "forwarded_port", guest: 80, host: 1234

  #Provisioning
  config.vm.provision "file",
    source: "~/Projects/files/git-config",
    destination: "~/.gitconfig"
  #Shell Script
  config.vm.provision "shell", 
    path: "~/Projects/scripts/lampstack.sh"

end
