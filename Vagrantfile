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
    v.keymap = 'en-gb'
    v.memory = 8192
    v.machine_virtual_size = 20
    end
  config.vm.provision "file", source: "~/Downloads/kea-premium-1.7.10.tar", destination: "$HOME/kea-premium-1.7.10.tar"
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/kea-dhcp-server.yml"
    end
  end
end
