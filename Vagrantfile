# -*- mode: ruby -*-
# vi: set ft=ruby :

ENV['VAGRANT_DEFAULT_PROVIDER'] = 'libvirt'


Vagrant.configure("2") do |config|

  ##### DEFINE VM #####
  config.vm.define "cent-01" do |config|
  config.vm.hostname = "cent-01"
  config.vm.box = "centos/8"
  config.vm.box_check_update = false
  config.vm.provider :libvirt do |v|
    v.cpus = 16
    v.memory = 8192
    v.machine_virtual_size = 20
    end
  end
end
