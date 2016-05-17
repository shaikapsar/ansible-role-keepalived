Keepalived Role
=========

Configure and start Keepalived in a docker container using the image `indigodatacloud/keepalived:latest`. 

This role has been specifically developed to be used in the framework of INDIGO-DataCloud project.

Role Variables
--------------

- `load_balancers_list` (optional): list of load balancer nodes - alternatively, you can use a proper inventory file specifying the hosts group [load_balancers]

- `keepalived_version` (default: latest)
- `keepalived_image` (default: indigodatacloud/keepalived:{{keepalived_version}}) 


Dependencies
------------

- `indigo-dc.docker`

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: indigo-dc.keepalived, load_balancers_list: ["10.10.10.1", "10.10.10.2"] }

License
-------

Apache Licence v2 [1]

[1] http://www.apache.org/licenses/LICENSE-2.0
