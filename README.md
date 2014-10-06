# Vagrant Node Red with Freeboard

This is a [Vagrant](http://vagrantup.com/)/[Ansible](http://www.ansible.com/) setup for running [node red](http://nodered.org/) in conjunction with the [freeboard](http://freeboard.io/) dashboard.

Inspired by this [Gist](https://gist.github.com/dceejay/fb47301b759222e05f84).

## Installation / Usage


Install Vagrant and Ansible on your platform.
Run

    vagrant up

Point your browser to [freeboard dashboard](http://localhost:1880/) to see the plain dashboard, to [freeboard websocket demo](http://localhost:1880/?load=demo_websocket_counter.json) to see the websocket counter demo and to [Node Red](http://localhost:1880/admin/) to access the Node Red configuration interface.

Uses upstart to start node red application.

Modify the vars http_port, install_path and run_as in the ansible playbook, if you want to use the playbook for installation on a non-vagrant machine.

## Installation on Beaglebone Black

The Ansible playbook can be used to install Node Red / Freeboard on a [Beaglebone Black](http://beagleboard.org/). Comment the variables for the Vagrant setup and uncomment the BBB settings. Hook up your BBB via USB as described in the [Getting Started](http://beagleboard.org/getting-started) Section of the BBB website.

Append your ssh pubkey to the .ssh/authorized_keys file of the debian user on the BBB and test the login.

Create an inventory file with only the IP address 192.168.7.2 in it.

Run

    ansible-playbook -i ../inventory provisioning/playbook.yml

This takes a while. If everything went ok Node Red should be available [here](http://192.168.7.2:1880/admin/). This setup was tested with a BBB that had already been in use. If you run into any problems please leave a description in the issues.
