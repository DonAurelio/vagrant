# Vagrant Single Machine

This Vagrantfile specifies the deployment of a single Virtual Machine.

### Getting Started

Clone this repository in your PC.

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

When you use ``vagrant ssh`` vagrant know how to authenticate into the master machines using the ssh-config data. So you don't need to know the password of each machine to log into it. 

```sh
vagrant ssh-config
```

```sh
Host default                                                                                             
  HostName 127.0.0.1                                                                                     
  User vagrant                                                                                           
  Port 2222                                                                                              
  UserKnownHostsFile /dev/null                                                                           
  StrictHostKeyChecking no                                                                               
  PasswordAuthentication no                                                                              
  IdentityFile /home/username/Desktop/projects/vagrant/single_machine/.vagrant/machines/default/virtualbox
/private_key                                                                                             
  IdentitiesOnly yes                                                                                     
  LogLevel FATAL  
```



