# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos64-lnpp"
  config.vm.box_url = "https://dl.dropbox.com/s/1vx4gd0jjbv69dr/SportIS-CentOS-6.4.box"

  config.vm.network :forwarded_port, guest: 80, host: 8080
  config.vm.network :forwarded_port, guest: 3306, host: 3306
  config.vm.network :private_network, ip: "192.168.3.3"

  config.vm.synced_folder "srv", "/srv", :nfs => true

  config.vm.provision :shell, :inline => "service nginx start"
end
