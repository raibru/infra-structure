# K3S Cluster for development infra structure

- use K§S as kubenernetes maintenance for container under development
- use vagrant to setup development infra structure
  - build VM with one master
  - build VM with n workers as node manged by master. Configured with 3 nodes
  - build VM with a docker registry service at port 5000
- use NFS to collect data hosted by server master
- include tools monitor system an network
- use tshark capture as system service in all VMs 
- access VMs via ssh connection

## Prerequisite

- use virtualbox with ubuntu boxes startup and setup VMs
- use vagrant to manage VMs in virtualbox
- use ansible to setup and maintain VMs configurations
- use ansible roles hosted at github.com:raibru/infra-structure/ansible-roles


