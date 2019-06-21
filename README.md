This scripts:

1) Create 2 VMs on Vagrant/VirtualBox from centos/7 box.
2) Add epel and jenkins repository to host1, install jenkins
3) Add epel repository to host2, install maven, add user for slave configuration.

TODO:
1) Make post install jenkins configuration 
2) Configure host2 as slave node
3) Add job to jankins and build it on slave.
