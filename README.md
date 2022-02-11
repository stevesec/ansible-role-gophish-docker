Ansible Gophish (Docker)
=========
[![CI](https://github.com/warhorse/ansible-role-gophish-docker/workflows/CI/badge.svg?event=push)](https://github.com/warhorse/ansible-role-gophish-docker/actions?query=workflow%3ACI)
[![warhorse.gophish_docker](https://img.shields.io/ansible/role/57577)](https://galaxy.ansible.com/warhorse/gophish_docker)
[![warhorse.gophish_docker](https://img.shields.io/ansible/quality/57577)](https://galaxy.ansible.com/warhorse/gophish_docker)
[![warhorse.gophish_docker](https://img.shields.io/ansible/role/d/57577)](https://galaxy.ansible.com/warhorse/gophish_docker)
![License](https://img.shields.io/github/license/warhorse/ansible-role-gophish-docker)
![Commit](https://img.shields.io/github/last-commit/warhorse/ansible-role-gophish-docker)

![Gophish Logo](./images/gophish_logo.png "Gophish Logo")


Install Gophish (Docker)

This role is part of the Warhorse Automation Framework. This role can be used with Warhorse or as a standalone role.

Docker Image
-------------

[Gophish](https://hub.docker.com/r/gophish/gophish)

Role Variables
--------------

A list of all the variables can be found in ./defaults/main.yml.

`gophish_dir` - gophish container directory 

`gophish_docker_version` - gophish image version

`gophish_ports` - gophish container ports

`gophish_hostname` - gophish container hostname

`gophish_container_name` - gophish container name 

`gophish_docker_image` - gophish docker image

`gophish_docker_network` gophish container docker network

Dependencies
------------

```shell
ansible-galaxy install geerlingguy.docker geerlingguy.pip
```

Install
------------

```shell
ansible-galaxy install warhorse.gophish_docker
```

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
      - { role: warhorse.gophish_docker }
```

Example Vars
----------------

```yaml
gophish_hostname: "gophish"
gophish_container_name: "gophish"
gophish_docker_version: "latest"
gophish_docker_labels: {}
gophish_docker_network: "gophish"
gophish_dir: '/opt/docker/gophish'
gophish_ports:
  - "80:80"
  - "443:443"
```

License
-------

MIT/BSD

Author Information
------------------

Ralph May
