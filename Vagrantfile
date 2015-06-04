# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"
    config.vm.box_url = "https://github.com/kraksoft/vagrant-box-ubuntu/releases/download/14.04/ubuntu-14.04-amd64.box"
  config.vm.provision :shell, :path => "minecraft_bootstrap"
  config.vm.provider "virtualbox" do |v|
     v.memory = "2048"
     v.customize [
         "modifyvm", :id,
         "--cpus", 2
#         "--pae", "on",
     ]
  end

  config.vm.network "public_network", bridge: 'eth0'
  config.vm.hostname ="minecraft.local"
end
