# WAVE - WordPress in Ansible for Vagrant and Everywhere

WAVE is an exploration in using Ansible as a provisioner for a nice WordPress setup. The initial focus will be in creating a virtual environment in Vagrant. The secondary focus will be to expand that environment to a production server as well.

## Getting Started

1. Install Virtualbox 4.2.18
1. Install Vagrant 1.3.1
1. `vagrant plugin install vagrant-hostsupdater`
1. `brew install ansible`
1. Get this repo in a directory
1. `vagrant up`

**Notes:**

* If you are using Windows or Linux, you'll need to replace the `brew install ansible` command with whatever it takes to get [Ansible](http://ansible.cc) installed on your host machine.
* The vagrant-hostsupdater plugin is nice, but not necessary.

## Current Status

1. Visiting [http://wave.dev](http://wave.dev) will give you an Nginx welcome screen
1. Visiting [http://10.10.99.99](http://10.10.99.99) will give you an Nginx welcome screen
1. Nothing else.