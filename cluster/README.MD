# Vagrant Single Machine

Deploy a single Virtual Machine

### Getting Started

Start cluster

```sh
vagrant up
```

Get into the machine

```sh
vagrant ssh
```

Stop virtual machine

```sh
vagrant halt
```

Destroy virtual machine

```sh
vagrant destroy
```

### Share Files (Virtual Machine and Host)

Vagrant enable by default a directory in to the Virtual Machine **/vagrant** which is shared with the folder on which the Vagrantfile resides in the Host.

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

Host slave_1
  HostName 127.0.0.1
  User vagrant
  Port 2200
  ...
  IdentityFile /home/username/Desktop/vagrant/cluster/.vagrant/machines/slave_1/virtualbox/private_key
  ...

Host slave_2
  HostName 127.0.0.1
  User vagrant
  Port 2201
  ...
  IdentityFile /home/username/Desktop/vagrant/cluster/.vagrant/machines/slave_2/virtualbox/private_key
  ...
```



