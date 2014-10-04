# Vagrant Node Red with Freeboard

This is a [Vagrant](http://vagrantup.com/)/[Ansible](http://www.ansible.com/) setup for running [node red](http://nodered.org/) in conjunction with the [freeboard](http://freeboard.io/) dashboard.

Inspired by this [Gist](https://gist.github.com/dceejay/fb47301b759222e05f84).

## Installation / Usage


Install Vagrant and Ansible on your platform.
Run

    vagrant up

Point your browser to [http://localhost:1880/] to see the plain dashboard, to [http://localhost:1880/?load=demo_websocket_counter] to see the websocket counter demo and to [http://localhost:1880/admin/] to access the Node Red configuration interface.

Uses upstart to start node red application.
