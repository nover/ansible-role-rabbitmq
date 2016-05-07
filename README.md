RabbitMQ
=========

A simple role that installs RabbitMQ from RabbitMQ's repositories on Ubuntu machines.

Build status https://travis-ci.org/nover/ansible-role-rabbitmq.svg?branch=master
Requirements
------------

No requirements except a Ubuntu machine to receive RabbitMQ and ansible it self

Role Variables
--------------

Per default the management plugin for rabbit mq will be enabled, and a global admin user with username "admin" and password "admin" will be created. The variables controlling this are the following:
```yaml
rabbitmq_enable_management_plugin: True
rabbitmq_admin_username: 'admin'
rabbitmq_admin_password: 'admin'
```

If you wish to change this behavior create a new local vars file, or pass in the variables as shown below.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
 - hosts: servers
   roles:
     - { role: nover.rabbitmq, rabbitmq_enable_management_plugin: False }
```

Or through a vars file:
```yaml
- hosts: servers
  roles:
    - { role: nover.rabbitmq}
  vars_files:
    - vars/rabbitmq.yml 
```

License
-------

Github The Unlicense (do whatever you want with the source)