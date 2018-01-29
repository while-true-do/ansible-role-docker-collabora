[![Build Status](https://travis-ci.org/while-true-do/ansible-role-docker-collabora.svg?branch=master)](https://travis-ci.org/while-true-do/ansible-role-docker-collabora)

# Ansible Role: Docker Collabora
| A role that runs the Collabora Online server as container using docker.

## Motivation

This role is needed to get the Collabora Online server running as docker container on the target machine.

## Installation

Install from [Ansible Galaxy](https://galaxy.ansible.com/while-true-do.docker-collabora)

```
ansible-galaxy install while-true-do.docker-collabora
```

Install from [Github](https://github.com/while-true-do/ansible-role-docker-collabora)

```
git clone https://github.com/while-true-do/ansible-role-docker-collabora.git while-true-do.docker-collabora
```

## Requirements

**Used Modules**

-   [docker_container](http://docs.ansible.com/ansible/latest/docker_container_module.html)

## Role Variables
```yaml
---
wtd_docker_collabora_image: "collabora/code"

wtd_docker_collabora_name: "collabora-online"

wtd_docker_collabora_ports: "127.0.0.1:9980:9980"
wtd_docker_collabora_domains: ""
wtd_docker_collabora_capabilities: "MKNOD"
```

## Dependencies

This role depends on <https://galaxy.ansible.com/while-true-do/docker>. You have to install the role:

```
ansible-galaxy install -r requirements.yml
```

## Example Playbook

Simple Example:

```yaml
- hosts: servers 
  roles:
    - { role: while-true-do.docker-collabora }
  vars:
    wtd_docker_collabora_domains: "collabora.example.com"
```

## Testing

All tests should be put in [test directory](./tests/).

## Contribute / Bugs

Thank you so much for considering to contribute. Every contribution helps us.
We are really happy, when somebody is joining the hard work. Please have a look
at the links first.

-   [Contribution Guidelines](./docs/CONTRIBUTING.md)
-   [Create an issue or Request](https://github.com/while-true-do/ansible-role-docker-collabora/issues)
-   [See who was contributing already](https://github.com/while-true-do/ansible-role-docker-collabora/graphs/contributors)

## License
This work is licensed under a [BSD License](https://opensource.org/licenses/BSD-3-Clause).

## Author Information

Blog: [blog.while-true-do.org](https://blog.while-true-do.org)

Mail: [hello@while-true-do.org](mailto:hello@while-true-do.org)
