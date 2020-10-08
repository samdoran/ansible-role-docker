Docker
=========
[![Galaxy](https://img.shields.io/badge/galaxy-samdoran.docker-blue.svg?style=flat)](https://galaxy.ansible.com/samdoran/docker)
[![Build Status](https://travis-ci.org/samdoran/ansible-role-docker.svg?branch=master)](https://travis-ci.org/samdoran/ansible-role-docker)

Install Docker CE.

Requirements
------------

RHEL: `rhel-7-server-extras-rpms` repo enabled
CentOS: `extras` repo enabled

Role Variables
--------------

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `docker_service_name` | `docker` | Service name to start/stop. |
| `docker_group` | `docker` | Name of the group users will be added to in order to be able to run Docker commands |
| `docker_edition` | `ce` | Which Docker editon to install. Options are `ce` or `ee` |
| `docker_users` | `[]` | List of users to add to `docker_group` |
| `docker_compose_install` | `yes` | Whether or not to install Docker Compose |
| `docker_compose_version` | `1.23.1` | Docker Compose version to install |
| `docker_compose_path` | `/usr/local/bin/docker-compose` | Path to install [Docker Compose](https://docs.docker.com/compose/overview/) binary |


Dependencies
------------

None

Example Playbook
----------------

    - hosts: all
      roles:
         - samdoran.docker

License
-------

MIT
