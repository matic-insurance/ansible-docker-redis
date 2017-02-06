Role Name
=========
[![Build Status](https://travis-ci.org/matic-insurance/ansible-docker-postgres.svg?branch=master)](https://travis-ci.org/matic-insurance/ansible-docker-postgres)

Ansible role to manage and run the redis docker container. It uses data container for persistence, which is more elegant way comparing to host volumes.

Requirements
------------

This role uses Ansible's docker module, so requirements are [the same](https://docs.ansible.com/ansible/docker_image_module.html#requirements-on-host-that-executes-module).

Role Variables
--------------

Here is the list of default variables with default values:

```
redis_docker_image: 'redis'
redis_docker_image_tag: '3-alpine'
redis_container_name: 'redis'
redis_port: 6379
```


Docker tuning can be done with these variables:
```
container_memory_limit: 512m
```

Dependencies
------------

No dependencies

Example Playbook
----------------

    - hosts: redis
      roles:
        - role: matic-insurance.docker-redis
          tags: ['redis']
          redis_container_name: 'my-redis'

License
-------

MIT

Author Information
------------------

Matic is a communication platform that connects lenders and borrowers originating a new home loan. A borrower now knows where they are in the loan process and what they need to do to complete the loan.
