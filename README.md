Custom Service-Golang Ansible Role
===============================

This role creates

Dependencies
------------

None.

Use this out of the box
=======================

To install all the defaults:

```
- hosts: my_server
  roles:
      - { role: custom_service_go }
```

Defining Variables
==================

You can provide a variable sector for your host like this:

Example of `host_vars/my_serever`

```
---
services:
  - name: gh-service
    clientID: 'our_id'
    clientSecret: 'our_secret'
    port: 3336
    scopes:
      - \"user:email\"
      - repo
user: 'vagrant'
group: 'vagrant'
go_path: "{{ ansible_env.HOME }}/go"

```

That will create a file in /etc/{{ services.name }}.conf with the provided yaml
(necessary to run the service executable.

The very basic Variables:
-------------------------
( Check out `defaults/main.yml` for advanced variables )

Author Information
==================

This role is provided by the [Tinkerware](http://tinkerware.io) project
under a **GNU GPLv3** Licence.
