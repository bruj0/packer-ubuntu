# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.ssh.insert_key = false
    #config.vm.synced_folder '.', '/shared', type: 'nfs'
    #config.vm.network "private_network", type: "dhcp"
  
    # VirtualBox.
    config.vm.define "virtualbox" do |virtualbox|
      virtualbox.vm.hostname = "virtualbox-ubuntu1804"
      virtualbox.vm.box = "file://box/virtualbox/ubuntu-18.04-0.1.box"

  
      config.vm.provider :virtualbox do |v|
        v.gui = true
        v.memory = 1024
        v.cpus = 1
        v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
        v.customize ["modifyvm", :id, "--ioapic", "on"]
      end
  
    end
  
  end