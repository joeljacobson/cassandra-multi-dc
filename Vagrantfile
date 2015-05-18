# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "precise64"
    config.vm.box_url = "http://files.vagrantup.com/precise64.box"

   config.vm.define "node1" do |node1|
    node1.vm.box = "precise64"
    node1.vm.network  "private_network", ip: "192.168.56.10"
    node1.vm.hostname = "node1"
  end

   config.vm.define "node2" do |node2|
    node2.vm.box = "precise64"
    node2.vm.network  "private_network", ip: "192.168.56.20"
    node2.vm.hostname = "node2"
  end

   config.vm.define "node3" do |node3|
    node3.vm.box = "precise64"
    node3.vm.network  "private_network", ip: "192.168.56.30"
    node3.vm.hostname = "node3"
  end

     config.vm.define "node4" do |node4|
      node4.vm.box = "precise64"
      node4.vm.network  "private_network", ip: "192.168.56.40"
      node4.vm.hostname = "node4"
    end

     config.vm.define "node5" do |node5|
      node5.vm.box = "precise64"
      node5.vm.network  "private_network", ip: "192.168.56.50"
      node5.vm.hostname = "node5"
    end

     config.vm.define "node6" do |node6|
      node6.vm.box = "precise64"
      node6.vm.network  "private_network", ip: "192.168.56.60"
      node6.vm.hostname = "node6"
    end

   config.vm.provision "ansible" do |ansible|
    ansible.playbook = "site.yml"
  end

    config.vm.define "opscenter" do |opscenter|
      opscenter.vm.box = "precise64"
      opscenter.vm.network  "private_network", ip: "192.168.56.70"
    end

    config.vm.provision "ansible" do |ansible|
     ansible.playbook = "tasks/opscenter.yml"
   end

 config.vm.provider "virtualbox" do |vb|
  vb.customize ["modifyvm", :id, "--memory", "2048"]
end

end
