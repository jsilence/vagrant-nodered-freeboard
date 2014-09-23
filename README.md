# Vagrant Node Red with Freeboard

This is a [Vagrant](http://vagrantup.com/)/[Ansible](http://www.ansible.com/) setup for running [node red](http://nodered.org/) in conjunction with the [freeboard](http://freeboard.io/) dashboard.

Inspired by this [Gist](https://gist.github.com/dceejay/fb47301b759222e05f84).

## Installation / Usage


Install Vagrant and Ansible on your platform.
Run

    vagrant up

Point your browser to [http://localhost:11880/] to see the dashboard and to [http://localhost:11880/admin/] to access the Node Red configuration interface.

## Issues / ToDos

Websockets are not working on the freeboard side. Trying to get it running with socket.io.

Make both Node Red and freebard load a preconfigured workflow and dashboard

Node Red has to be started manually. Configure supervisord to start Node Red when the VM starts.
