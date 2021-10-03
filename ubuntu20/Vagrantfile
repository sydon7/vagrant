# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.synced_folder '.', '/vagrant'

  config.vm.provider "virtualbox" do |vb|
      vb.memory = "2024"
  end 

  #config.vm.synced_folder '.', '/vagrant', nfs: true

  config.vm.define "myvm" do |myvm|
      myvm.vm.host_name = "myvm"

      # bootstrap the VM a few packages, specifically ansible
      myvm.vm.provision "shell", inline: <<-SHELL
       apt-get update
       apt-get install -y python3-pip
       pip3 install -r /vagrant/requirements.txt 
      SHELL

      # now use ansible to finish the build
      myvm.vm.provision "ansible" do |ansible|
          ansible.playbook = "build.yml"
      end
  end
end

