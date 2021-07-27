Docker
=========
[![Galaxy](https://img.shields.io/badge/galaxy-samdoran.docker-blue.svg?style=flat)](https://galaxy.ansible.com/samdoran/docker)

Install Docker CE.

Requirements
------------

- `docker` Python SDK installed on managed node

Role Variables
--------------

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `docker_service_name` | `docker` | Service name to start/stop. |
| `docker_group` | `docker` | Name of the group users will be added to in order to be able to run Docker commands |
| `docker_edition` | `ce` | Which Docker editon to install. Options are `ce` or `ee` though only `ce` works currently. |
| `docker_users` | `[]` | List of users to add to `docker_group` |
| `docker_compose_install` | `yes` | Whether or not to install Docker Compose |
| `docker_compose_version` | `1.26.0` | Docker Compose version to install |
| `docker_compose_path` | `/usr/local/bin/docker-compose` | Path to install [Docker Compose](https://docs.docker.com/compose/overview/) binary |
| `docker_yum_repositories` | `[see defaults/main.yml]` | Docker repositories used on RHEL distributions.  |
| `docker_daemon_config` | `~` | Dictionary of settings that will be converted to JSON and put in `/etc/docker/daemon.json`. Make sure these options are valid or Docker will fail to start. With the default value, this file will be removed. |


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

Apache 2.0
