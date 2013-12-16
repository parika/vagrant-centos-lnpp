# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "lnpp"
  # config.vm.box_url = "http://domain.com/path/to/above.box"

  config.vm.network :private_network, ip: "192.168.2.2"

  config.vm.network :forwarded_port, guest: 80, host: 8080
  config.vm.network :forwarded_port, guest: 8080, host: 8181
  config.vm.network :forwarded_port, guest: 3306, host: 3306

  config.vm.synced_folder "srv", "/srv", :nfs => true

  config.vm.provision :shell, :inline => "service nginx restart"
end
