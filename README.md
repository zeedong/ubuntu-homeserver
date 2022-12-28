# Ansible Ubuntu setup
Ansible roles to setup Ubuntu server, this playbook is focused on quickly deploying a "ready to use" homeserver.
copy and simplify from this project: [ubuntu asible](https://github.com/lvancrayelynghe/ansible-ubuntu/blob/master/README.md)

## Requirements
- Git
- Ansible 2+ (automatically installed from [Ansible offical PPA](https://launchpad.net/~ansible/+archive/ubuntu/ansible) with the provided install.sh script)

## Installation
First, you need to install Git and Ansible :
```
sudo apt-get install git
git clone https://github.com/Benoth/ansible-ubuntu.git
cd ansible-ubuntu
./install.sh
```

Then you need to customize the playbook `ubuntu-homeserver-ansible.yml` (or create a new one) to suit your needs. Every roles are disabled by default.

Run `ansible-playbook ansible-desktop.yml --ask-become-pass` and enter your sudo password to run the playbook

## Roles included

| Role                     | Description                                                                                                                                                                                                                                                                                                                           |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| | **General** |
| common                   | Install a lot of usefull packages (curl, htop, less, zip ... see [corresponding task file](https://github.com/Benoth/ansible-ubuntu/blob/master/roles/common/tasks/main.yml))                                                                                                                                                         |
| | **Services & server tools** |
| docker                   | Install [Docker](https://www.docker.com/) and Docker compose from Docker deb repository                
| portainer                | Install [Portainer and containers](https://medium.com/@dmarko484/ansible-docker-with-portainer-on-ubuntu-server-installation-45a69e07785c)
| ssh                      | Install [OpenSSH Server](http://www.openssh.com/)                                                                                                                                                                                                                                                                                     |

