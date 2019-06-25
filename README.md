CentOS 7 everythere.

This scripts:

1) Create 2 VMs on Vagrant/VirtualBox from centos/7 box.
2) Add epel and jenkins repository to host1, install some additional software, Jenkins
3) Create project and job on jenkins(just for echo command with every minute build), configure admin user, create Slave node. 
3) Add epel repository to host2, install maven and some additional software, add user for slave configuration, run slave agent with a secret using java.

TODO:
1) Improve work with Jenkins plugins(now it's working(but commented), but better use Jenkins cli) 
2) Start using git repo:  https://github.com/pdurbin/maven-hello-world for build.


