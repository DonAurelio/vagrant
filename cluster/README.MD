# Vagrant Cluster 

This Vagrantfile specifies the deployment of a Cluster of Virtual Machines (master,slave_1,slave_2) on which machines can communicate to each other. This kind of enviroments are desiable to perform distrubited computations on which machines needs to communicate to perform the compelete job.

### Getting Started

Clone this repository

```sh
git clone https://github.com/DonAurelio/vagrant.git
```

Get into the **cluster** configuration folder

```sh
cd vagrant/cluster
```

Start cluster

```sh
vagrant up
```

Get into the one machine of the cluster (master or slave)

```sh
vagrant ssh master
vagrant ssh slave
```

Stop cluster

```sh
vagrant halt
```

Destroy cluster

```sh
vagrant destroy
```

### Share Files (Virtual Machine and Host)

Vagrant enable by default a directory in to the Virtual Machines **/vagrant** which is shared with the folder on which the Vagrantfile resides in the Host.

### Further Information

See Virtual Machines SSH Settings

When you use ``vagrant ssh master`` vagrant know how to authenticate into the master machines using the ssh-config data. So you don't need to know the password of each machine to log into it. 

```sh
vagrant ssh-config
```

```sh
Host master
  HostName 127.0.0.1
  User vagrant
  Port 2222
  ...
  IdentityFile /home/username/Desktop/vagrant/cluster/.vagrant/machines/master/virtualbox/private_key
  ...

Host slave
  HostName 127.0.0.1
  User vagrant
  Port 2200
  ...
  IdentityFile /home/username/Desktop/vagrant/cluster/.vagrant/machines/slave_1/virtualbox/private_key
  ...
```



