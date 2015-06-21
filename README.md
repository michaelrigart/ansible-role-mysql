Ansible Mysql Role
==================
[![Build Status](https://semaphoreci.com/api/v1/projects/3f4eaa5c-6d48-4a16-8bd0-ed4d6450d566/461757/badge.svg)](https://semaphoreci.com/michaelrigart/ansible-role-mysql) [![Build Status](https://travis-ci.org/michaelrigart/ansible-role-mysql.svg?branch=master)](https://travis-ci.org/michaelrigart/ansible-role-mysql)

An ansible role for installing and configuring MySQL client / server

Role Variables
--------------

```yaml
mysql_server_install: define if you wish to install mysql server
mysql_server_pkg_version: define the mysql server version
mysql_server_pkg_state: installed
mysql_client_install: define if you wish to install mysql client
mysql_client_pkg_version: define the mysql client version
mysql_client_pkg_state: installed
mysql_service_state: define the mysql service state
mysql_service_enabled: define if the mysql service needs to be enabled
mysql_root_password: define the root password
mysql_root_config: holds a dictionary with all config parameters. See the defaults for an example
mysql_replication_user: list of replication users, containing name and password
mysql_role: define the role of the mysql instance ( master / slave ). Or omit when using standalone.
mysql_replication_master: define the replication master host. Omit when using standalone
```

Example Playbook
-------------------------

```yaml
- hosts: servers
  roles:
     - { role: MichaelRigart.mysql, sudo: Yes }
```

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>