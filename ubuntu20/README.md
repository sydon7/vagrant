# Simple example

Simple Vagrant file that builds a vm, installs ansible and a few python
packages as the user vagrant. 

* Ensure that vagrant is properly installed

* Ensure that ansible is installed

* Copy the Vagrantfile, build.yml and requirements.txt in into a directory

* build the VM with

```
vagrant up

```


* Connect to the VM, you should have a fully patched systems with alll the packages
and config defined in the build.yml playbook.



```

~/vagrant/ubuntu20-ansible$ vagrant ssh
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 5.4.0-88-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Sun Oct  3 19:25:47 UTC 2021

  System load:  0.47              Processes:               128
  Usage of /:   5.5% of 38.71GB   Users logged in:         0
  Memory usage: 17%               IPv4 address for enp0s3: 10.0.2.15
  Swap usage:   0%


0 updates can be applied immediately.


Last login: Sun Oct  3 19:22:50 2021 from 10.0.2.2
vagrant@myvm:~$ which ansible
/home/vagrant/.local/bin/ansible
vagrant@myvm:~$ pip3 list | grep netaddr
netaddr                0.8.0               


```
