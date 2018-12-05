# zabbix

[![Build Status](https://travis-ci.com/iroquoisorg/ansible-role-zabbix.svg?branch=master)](https://travis-ci.com/iroquoisorg/ansible-role-memcached)

Ansible role for zabbix

This role was prepared and tested for Ubuntu 16.04.

# Installation

`$ ansible-galaxy install iroquoisorg.zabbix`

# Default settings

```

zabbix_version: 3.4
zabbix_database_type: mysql
zabbix_domain: zabbix.local
zabbix_email_from: zabbix@example.com
zabbix_server_listenport: 10051
zabbix_slack_username: Zabbix

zabbix_db: 'zabbix'
zabbix_db_host: '127.0.0.1'
zabbix_db_user: 'zabbix'
zabbix_db_pass: 'zabbix'

databases: [ "{{ zabbix_db }}" ]
mysql_users: [
    {
      name: "{{ zabbix_db_user }}",
      password: "{{ zabbix_db_pass }}",
      database: "{{ zabbix_db_pass }}"
    }
  ]

```

# Development

Please check [development guide](DEVELOPMENT.md) for details about developing and testing this role.
