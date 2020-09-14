# -*- mode: ruby -*-
# vi: set ft=ruby :

ENV['VAGRANT_DEFAULT_PROVIDER'] = 'libvirt'


Vagrant.configure("2") do |config|

  ##### DEFINE VM #####
  config.vm.define "cent-01" do |config|
  config.vm.hostname = "cent-01"
  config.vm.box = "centos/7"
  config.vm.box_check_update = false
  config.vm.provider :libvirt do |v|
    v.memory = 4096
    end
  end
end
