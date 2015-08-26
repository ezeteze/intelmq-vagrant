# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "private_network", ip: "192.168.33.10"
  config.ssh.forward_agent = "true"
  config.vm.provider "virtualbox" do |vb|
     vb.memory = "4024"
     vb.cpus = "4"
  end
  config.vm.provision "ansible" do  |ansible|
         ansible.playbook = "intelmq-elk/site.yml"
         ansible.sudo = "true"
  end
end
