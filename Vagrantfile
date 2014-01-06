# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.hostname = "magic-berkshelf"
  config.vm.box = "opscode-ubuntu-12.04"
  config.vm.box_url = "https://opscode-vm-bento.s3.amazonaws.com/vagrant/opscode_ubuntu-12.04_provisionerless.box"

  config.berkshelf.enabled = true
  config.omnibus.chef_version = :latest

  config.vm.network :forwarded_port, guest: 80, host: 8080

  config.vm.provision :chef_solo do |chef|
    chef.run_list = [
      "recipe[apt]",
      "recipe[magic::default]"
    ]
  end
end
