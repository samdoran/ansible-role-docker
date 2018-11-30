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
