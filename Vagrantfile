# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.hostname = "magic-berkshelf"
  config.vm.box = "chef-magic"
  config.vm.box_url = "https://opscode-vm-bento.s3.amazonaws.com/vagrant/boxes/opscode_ubuntu-12.04_provisionerless.box"

  config.ssh.max_tries = 40
  config.ssh.timeout   = 120
  config.berkshelf.enabled = true
  config.omnibus.chef_version = :latest

  config.vm.provision :chef_solo do |chef|
    chef.run_list = [
      "recipe[apt]",
      "recipe[magic::default]"
    ]
  end
end
