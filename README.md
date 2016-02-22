OpenBazaar
=========

[![Build Status](https://api.travis-ci.org/tyler-smith/ansible-openbazaar.png)](https://api.travis-ci.org/tyler-smith/ansible-openbazaar.png)

OpenBazaar server installation

Role Variables
--------------

Available vars and their defaults listed below.

```yaml
---
openbazaar_git_url: https://github.com/OpenBazaar/OpenBazaar-Server.git
openbazaar_git_version: master

openbazaar_group: openbazaar
openbazaar_user: openbazaar
openbazaar_user_home_directory: /home/openbazaar

openbazaar_executable: openbazaard.py
openbazaar_log_path: /var/log/openbazaar

openbazaar_service_name: openbazaar

openbazaar_dht_port: 28467

openbazaar_additional_flags: -t

```

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - { role: openbazaar }
```

License
-------

BSD

Author Information
------------------

Tyler Smith - tylersmith.me@gmail.com
