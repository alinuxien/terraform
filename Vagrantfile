# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "terraform" do |terraform|
    terraform.vm.box = "hashicorp/bionic64"
    terraform.vm.box_version = "1.0.282"
    terraform.vm.hostname = "terraform"
    terraform.vm.network "forwarded_port", guest: 22, host: 2222
    terraform.vm.provider "virtualbox" do |v|
      v.name = "terraform-vieillot"
      v.memory = 4096
      v.cpus = 4
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
      v.customize [ "guestproperty", "set", :id, "/VirtualBox/GuestAdd/VBoxService/--timesync-set-threshold", 10000 ]
    end
    terraform.vm.provision :shell, path: "bootstrap.sh"
    terraform.vm.provision :shell, path: "auto_cd.sh"
  end
end

