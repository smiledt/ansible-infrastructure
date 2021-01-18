# Ansible Docker Networking

An Ansible role that creates a user-defined Docker networks

Requires Docker to be installed first.

##  Requirements

N/A

## Role Variables

`docker_networks`: Dictionary list of docker networks matching https://docs.ansible.com/ansible/latest/modules/docker_network_module.html

## Dependencies

- Docker

## Example Playbook

```yaml
- hosts: servers
  become: true
  roles:
    - role: calvinbui.ansible_docker
    - role: calvinbui.ansible_docker_network
```

## License

GPLv3

## Author Information

http://calvin.me
