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
