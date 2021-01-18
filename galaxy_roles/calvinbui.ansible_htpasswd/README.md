# Ansible htpasswd

Add and remove username/password entries in a password file using htpasswd.

##  Requirements

N/A

## Role Variables

`htpasswd_users`: A list users to add. [All available options used in the htpasswd module can be used here as well](https://docs.ansible.com/ansible/latest/modules/htpasswd_module.html). Set it exactly the same as the htpasswd module, e.g.

```
htpasswd_users:
  - name: janedoe
    password: '9s36?;fyNp'
    owner: root
    group: www-data
    mode: 0640
    path: /etc/nginx/passwdfile
  - name: foobar
    state: absent
    path: /etc/nginx/passwdfile
  - name: alex
    password: oedu2eGh
    crypt_scheme: md5_crypt
    path: /etc/nginx/passwdfile
  - ...
```

## Dependencies

passlib

## Example Playbook

```yaml
- hosts: servers
  become: true
  pre_tasks:
    - name: Update apt cache.
      apt:
        update_cache: true
        cache_valid_time: 600
      changed_when: false
  roles:
   - role: ansible-htpasswd
```

## License

GPLv3

## Author Information

http://calvin.me
