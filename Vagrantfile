# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y build-essential libaio1
    cp /vagrant/v11.1_linuxx64_expc.tar.gz expc.tar.gz
    tar -xzf expc.tar.gz
    ./expc/db2setup -r response_file.rsp
  SHELL
end
