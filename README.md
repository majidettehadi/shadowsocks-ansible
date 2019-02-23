Shadowsocks
=========

Install and config shadowsocks client service.

Role Variables
--------------

Settable variables for this role:
* **shadowsocks_local_port**: Port which client accept connections.
* **shadowsocks_local_address**: Network address which client accept connections example: 127.0.0.1, 0.0.0.0, 10.10.0.0/16 
* **shadowsocks_config_name**: File name of config file which contains shadowsocks_server and shadowsocks_password vars. This file must be at vars directory and I suggest to use ansible vault to create file with encryption.
* **shadowsocks_server**: Shadowsocks server address.
* **shadowsocks_password**: Shadowsocks server password.

Example Playbook
----------------

To run this role correctly you must create a file in vars directory (with ansible vault) which contains shadowsocks_server and shadowsocks_password vars.
Then create a playbook like this:
    
    - hosts: servers
      roles:
        - { role: majidettehadi.shadosocks, tags: shadowsocks }

Run with vault password:

    ./playbook.yml -t shadowsocks --vault-password-file=secrets/shadowsocks

License
-------

BSD

Author Information
------------------

Seyedmajid Etehadi
ettehadi.m@gmail.com
