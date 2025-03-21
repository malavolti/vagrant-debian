# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # VM hostname
  # https://developer.hashicorp.com/vagrant/docs/networking/basic_usage
  config.vm.hostname = "vm.local"

  # Every Vagrant development environment requires a box. 
  # You can search for boxes at https://vagrantcloud.com/search.
  config.vm.box = "debian/bookworm64"

  # Enable automatic box update checking. This is recommended.
  config.vm.box_check_update = true

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # NOTE: This will enable public access to the opened port
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine and only allow access
  # via 127.0.0.1 to disable public access
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # https://developer.hashicorp.com/vagrant/docs/networking/basic_usage
  # config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "private_network", ip: "192.168.33.10", hostname: true

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Data will be shared by the /vagrant VM directory

  config.vm.provider :libvirt do |vm|
    vm.cpus = 2
    vm.memory = 1024
  end

  # This is the username that Vagrant will use when attempting any sort of SSH-based communication with the VM.
  config.ssh.username = "vagrant"

  # Enable provisioning with a shell script. Additional provisioners such as
  # Ansible, Chef, Docker, Puppet and Salt are also available. Please see the
  # documentation for more information about their specific syntax and use.
  config.vm.provision "shell", inline: <<-SHELL
    export DEBIAN_FRONTEND=noninteractive
    apt-get update
    apt-get upgrade --yes
  SHELL

end
