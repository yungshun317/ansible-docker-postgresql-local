# Ansible Docker Postgres Local
[![Work with Ansible](https://img.shields.io/badge/Work%20with-Ansible-brightgreen.svg)](https://img.shields.io/badge/Work%20with-Ansible-brightgreen.svg) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) 

An Ansible playbook deploys PostgreSQL on a Docker container locally. For remote hosts, please see my another project, [Ansible Docker Postgres Remote](https://github.com/yungshun317/ansible-docker-postgres-remote).

## Requirements

|Package|Version|  
|:-----:|:-----:|  
|python2|2.7.12|  
|ansible|2.7.2|  
|docker|18.09.6|

## Usage
Run `ansible-playbook`. 
```sh
$ ansible-playbook postgres.yml
```

## Outline
The playbook simply does these locally:
1. Install `pip`, `docker-io` with `apt`.
2. Install Docker Python library with `pip`.
3. Build Docker images, `db` and `data`, from Dockerfiles with the `docker_image` module.
4. Use the Ansible `docker_container` module to run containers.

## Tech
This project uses:
* [Ansible](https://www.ansible.com/) - Ansible is open source software that automates software provisioning, configuration management, and application deployment.
* [Docker](https://github.com/docker/docker-ce) - a computer program that performs operating-system-level virtualization, also known as containerization.

## Todos
 - Try to write an Ansible Role.

## License
[Ansible Docker Postgres Local](https://github.com/yungshun317/ansible-docker-postgres-local) is released under the [MIT License](https://opensource.org/licenses/MIT) by [yungshun317](https://github.com/yungshun317).
