# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.synced_folder "services", "/srv", type: "rsync", rsync__auto: true
  config.vm.provision "ansible_local" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "provision.yml"
  end
end
