# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.provider :virtualbox do |v|
    v.customize ["modifyvm", :id, "--memory", 512]
  end

  config.ssh.forward_agent = true

  config.vm.box = "precise32"
  config.vm.box_url = "http://files.vagrantup.com/precise32.box"

  config.vm.hostname = "wave"

  if defined? VagrantPlugins::HostsUpdater
    config.hostsupdater.aliases = [
      "wave.dev"
    ]
  end

  config.vm.network :private_network, ip: "10.10.99.99"
 
  config.vm.provision :ansible do |ansible|
      ansible.playbook = "site.yml"
      ansible.verbose = true
      ansible.sudo = true
  end
end
