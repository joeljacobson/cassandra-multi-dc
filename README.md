##Introduction

Easily provision a multi-workload cluster running Cassandra and Spark with Opscenter using Ansible with Vagrant & Virtualbox.

*Disclaimer*: I use this for demo purposes only, nothing serious.

##Prerequisites

* [Virtualbox](https://www.virtualbox.org/)
* [Vagrant](https://www.vagrantup.com/downloads)
* [Ansible](http://docs.ansible.com/intro_installation.html)

##Provisioning

Clone the project: ```git clone https://github.com/joeljacobson/multi-dc-cluster.git```

In the project directory enter: ```vagrant up```

Your cluster will be ready shortly depending on your internet connection. The initial boot takes some time as Ansible has to download, install and configure DSE across each VM. Subsequent reboots are fast.

DSE and Opscenter will be automatically configured and started once installed. They will also be automatically started each time the VMs are booted.

Cassandra will be running on: ```192.168.56.10```, ```192.168.56.20```, ```192.168.56.30```
Spark will be running on ```192.168.56.40```, ```192.168.56.50```, ```192.168.56.60```

Opscenter will be running on: ```192.168.56.70:8888```

Install the datastax-agents by entering ```vagrant``` for both the username and password.

SSH into a node with: ```vagrant ssh <node$>```

Shutdown the VMs: ```vagrant halt```

Resume VMs: ```vagrant up```

Destroy the VMs (requires re-provisioning): ```vagrant destroy```
