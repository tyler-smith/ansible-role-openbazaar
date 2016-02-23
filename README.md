OpenBazaar
=========

[![Build Status](https://api.travis-ci.org/tyler-smith/ansible-openbazaar.png)](https://api.travis-ci.org/tyler-smith/ansible-role-openbazaar.png)

OpenBazaar Server Installation Role

Install
----------------

```sh
ansible-galaxy install tyler-smith.openbazaar
```

Role Variables and Defaults
--------------

```yaml
# Whether or not we want a full node or just a seed server
openbazaar_seed: false

# Git URL and version for the server code you want to run
openbazaar_git_url: https://github.com/OpenBazaar/OpenBazaar-Server.git
openbazaar_git_version: master

# Information for the OS user that will run the server
openbazaar_group: openbazaar
openbazaar_user: openbazaar
openbazaar_user_home_directory: /home/openbazaar

# DHT port setting
openbazaar_dht_port: 28467

# The username and password to use when connecting to the API
openbazaar_username: username
openbazaar_password: password

# Any additional flags. Defaults to testnet flag
openbazaar_additional_flags: -t


## Server specific
# Port settings
openbazaar_rest_port: 18469
openbazaar_websocket_port: 18466
openbazaar_heartbeat_port: 18470

# Address to allow API connects from
openbazaar_allowed_ip: 127.0.0.1

```

Example Playbook
----------------

```yaml
    - hosts: servers
      vars:
        openbazaar_username: myuser
        openbazaar_password: myp@ssw0rD
      roles:
         - tyler-smith.openbazaar
```

License
-------

[BSD](LICENSE)

Author Information
------------------

Tyler Smith - tylersmith.me@gmail.com
