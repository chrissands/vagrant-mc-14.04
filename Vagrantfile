# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.box_url = "http://files.vagrantup.com/trusty64.box"
  config.vm.provision :shell, :path => "minecraft_bootstrap"
  config.vm.provider "virtualbox" do |v|
     v.memory = "2048"

  end

  config.vm.network "public_network", bridge: 'eth0'
  config.vm.hostname ="minecraft.local"
end
