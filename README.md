ansible-influxdb-bucket
=======================

This role creates InfluxDB buckets and sets tokens.

Requirements
------------

A running InfluxDB endpoint with an admin token.

Role Variables
--------------


Dependencies
------------

N.A.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - role: ansible-influxdb-bucket
      vars:
         influxdb_api:
             token: secret
             endpoint: http://localhost:8086
             tokens_output_file: ~/.influxdb_tokens
         influxdb_buckets:
             - name: my-buc
               org: default
               retention_hours: 
               create_write_token: true
               create_read_token: true

License
-------

GPL-3+

Author Information
------------------

Mathieu GRZYBEK
