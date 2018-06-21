# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.require_version ">= 1.6.2"

BOX_NAME = "MacOSX_Sierra"

Vagrant.configure("2") do |config|
  config.vm.box = BOX_NAME
  config.vm.box = "jhcook/macos-sierra"
  config.vm.box_check_update = true
  config.vm.hostname = "macosx-sierra"
  config.vm.network :private_network, ip: "192.168.121.81" 
  config.vm.network :forwarded_port, guest: 80, host: 8180

  config.vm.provider :virtualbox do |vb|
     vb.gui = false
     vb.name = BOX_NAME
     vb.customize ["modifyvm", :id, "--memory", "8192"]
     vb.customize ["modifyvm", :id, "--cpus", "2"]
     vb.customize ["modifyvm", :id, "--usb", "on"]
     vb.customize ["modifyvm", :id, "--usbehci", "off"]
  end
end

