# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  #config.vm.box = "ubuntu/trusty64"
  config.vm.box_check_update = false


  config.vm.define "konev" do |konev|
    konev.vm.box = "hashicorp/precise32"
    konev.vm.network  "forwarded_port", guest: 80, host: 9900
    konev.vm.network  "forwarded_port", guest: 22, host: 9999
    konev.vm.provider "virtualbox" do |vb| 
      vb.customize ["modifyvm", :id, "--cableconnected1", "on"]
      vb.name = "konev"

    end
  end
end

