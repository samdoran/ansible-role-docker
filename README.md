Docker
=========
[![Galaxy](https://img.shields.io/badge/galaxy-samdoran.docker-blue.svg?style=flat)](https://galaxy.ansible.com/samdoran/docker)

Install Docker CE.

Requirements
------------

None.

Role Variables
--------------

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `docker_service_name` | `docker` | Service name to start/stop. |
| `docker_repo_file` | `docker-ce` | Repo file name on systems using `yum` |
| `docker_compose_install` | `true` | Whether or not to install Docker Compose |
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
