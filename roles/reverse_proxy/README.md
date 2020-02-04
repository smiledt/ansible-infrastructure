# reverse_proxy

## Table Of Contents

* [About](#about)
* [Role Defaults](#role-defaults)
* [License](#license)
* [Author](#author)

## About

> This role configures a reverse_proxy for my network infrastructure

[Back to table of contents](#table-of-contents)

## Role Defaults

**Quicklist**: [auth_ip](#auth_ip), [certbot_auto_renew](#certbot_auto_renew),
[certbot_auto_renew_hour](#certbot_auto_renew_hour),
[certbot_auto_renew_minute](#certbot_auto_renew_minute),
[certbot_auto_renew_options](#certbot_auto_renew_options),
[certbot_auto_renew_user](#certbot_auto_renew_user),
[certbot_create_command](#certbot_create_command),
[certbot_create_if_missing](#certbot_create_if_missing),
[certbot_create_method](#certbot_create_method), [certbot_create_standalone_sto
p_services](#certbot_create_standalone_stop_services),
[certbot_dir](#certbot_dir),
[certbot_install_from_source](#certbot_install_from_source),
[certbot_keep_updated](#certbot_keep_updated), [certbot_repo](#certbot_repo),
[certbot_version](#certbot_version), [dns_zone](#dns_zone)

### auth_ip 

* *help*: TODO.

[Back to table of contents](#table-of-contents)

### certbot_auto_renew 

* *help*: TODO.
* *default*: ``True``

[Back to table of contents](#table-of-contents)

### certbot_auto_renew_hour 

* *help*: TODO.
* *default*: ``3``

[Back to table of contents](#table-of-contents)

### certbot_auto_renew_minute 

* *help*: TODO.
* *default*: ``30``

[Back to table of contents](#table-of-contents)

### certbot_auto_renew_options 

* *help*: TODO.
* *default*: ``--quiet --no-self-upgrade``

[Back to table of contents](#table-of-contents)

### certbot_auto_renew_user 

* *help*: TODO.
* *default*: ``{{ mgmt_user }}``

[Back to table of contents](#table-of-contents)

### certbot_create_command 

* *help*: TODO.
* *default*: ``{{ certbot_script }} certonly --standalone --noninteractive --agree-tos --email {{ site_item.value.email | default(certbot_admin_email) }} -d {{ site_item.value.server_fqdn }}``

[Back to table of contents](#table-of-contents)

### certbot_create_if_missing 

* *help*: TODO.
* *default*: ``True``

[Back to table of contents](#table-of-contents)

### certbot_create_method 

* *help*: TODO.
* *default*: ``standalone``

[Back to table of contents](#table-of-contents)

### certbot_create_standalone_stop_services 

* *help*: TODO.
* *default*: 
  * ``nginx``

[Back to table of contents](#table-of-contents)

### certbot_dir 

* *help*: TODO.
* *default*: ``/opt/certbot``

[Back to table of contents](#table-of-contents)

### certbot_install_from_source 

* *help*: TODO.
* *default*: ``True``

[Back to table of contents](#table-of-contents)

### certbot_keep_updated 

* *help*: TODO.
* *default*: ``True``

[Back to table of contents](#table-of-contents)

### certbot_repo 

* *help*: TODO.
* *default*: ``https://github.com/certbot/certbot.git``

[Back to table of contents](#table-of-contents)

### certbot_version 

* *help*: TODO.
* *default*: ``master``

[Back to table of contents](#table-of-contents)

### dns_zone 

* *help*: TODO.

[Back to table of contents](#table-of-contents)

## License

license (GPL-2.0-or-later, MIT, etc)

[Back to table of contents](#table-of-contents)

## Author

Derek Smiley

Note: I am not claiming this to be original work, I got some of it from an ansible-galaxy role and other online resources. This is for educational purposes only.

[Back to table of contents](#table-of-contents)
