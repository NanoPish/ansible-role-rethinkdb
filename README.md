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

Address of local interfaces to listen on when accepting connections                                                                                                                                     │ gt_belin_front.yml
May be 'all' or an IP address, loopback addresses are enabled by default                                                                                                                                │ gt_belin_fro..date_nodejs.yml
Default: all local addresses


 `rethinkdb_joins:                                                                                                                                                                                     │ gt_cengage_bastion.yml
    - ip: 10.0.0.43                                                                                                                                                                                    │ gt_cengage_rethinkdb.yml
      port: 29015                                                                                                                                                                                      │ gt_creo_conv.yml
    - ip: 10.0.0.125                                                                                                                                                                                   │ gt_history.yml
      port: 29015`

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
         - rethinkdb
      
      vars:                                                                                                                                                                                                        │ gt_belin_pre..d_rethinkdb.yml
        rethinkdb_bind: all

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2019 by gpkfr.
