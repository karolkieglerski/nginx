nginx
=========

[![Build Status](https://travis-ci.org/kilerkarol/nginx.svg?branch=master)](https://travis-ci.org/kilerkarol/nginx)

Role install and configure nginx.

Role Variables
--------------

Default variables for that role
```
    nginx_purge: false
```

Variable set to get default ansible variable form inventory `ansible_port` 
```
    ssh_port: "{{ ansible_port }}"
```

Other variables for that role:
```
  nginx_version: "1.10.3"

  nginx_packages:
    - { name: "nginx", version: "{{ nginx_version }}", state: "present" }
```    

Example Playbook
----------------

```
  - hosts: servers
    roles:
      - { role: kilerkarol.nginx, tag: nginx }
```

License
-------

BSD

Author Information
------------------

Karol Kieglerski