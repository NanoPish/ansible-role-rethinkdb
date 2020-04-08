Ansible Role: Rethinkdb
=========

install and configure [Rethinkdb](https://rethinkdb.com) server (or in cluster) On GNU/Debian 10.

Requirements
------------

Compatible with Debian 10. `sudo`, `ca-certificates` and `apt-transport-https`must be available on the server.

Role Variables
--------------

Available variables are listed below :

  rethinkdb_datadir: /path/to_data

Directory to store data and metadata.

  rethinkdb_bind : all

Address of local interfaces to listen on when accepting connections
May be 'all' or an IP address, loopback addresses are enabled by default
Default: all local addresses


 rethinkdb_joins:
    - ip: 10.0.0.43
      port: 29015
    - ip: 10.0.0.125
      port: 29015

Array of host and port to connect to. (Cluster)

  rethinkdb_cache_size: 1024

Size of the cache in MB

  rethinkdb_nohttp: Yeah

If Present Disable web administration console (Port 8080)

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - gpkfr.rethinkdb
      
      vars:
        rethinkdb_bind: all

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2019 by gpkfr.
