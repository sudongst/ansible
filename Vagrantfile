# -*- mode: ruby -*-
# vi: set ft=ruby :

  #================#
  # Ansible Server #
  #================#
  
  Vagrant.configure("2") do |config|
    config.vm.define "ansible-server" do |cfg|
      cfg.vm.box = "centos/7" # '='가 필수적으로 필요 
    cfg.vm.provider "virtualbox" do |vb|
      vb.name = "Ansible-Server" # '='가 필수적으로 필요 
    end
    cfg.vm.host_name = "ansible-server" # '='가 필수적으로 필요 
    cfg.vm.network "public_network", ip: "192.168.56.10"
    cfg.vm.network "forwarded_port", guest: 22, host: 60010, auto_correct: true, id: "ssh"
    cfg.vm.synced_folder "../data", "/vagrant", disabled: true
    end
  end
