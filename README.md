Ansible Role: Webmin
====================

Install and configure Webmin for:

- Debian (12/13)
- Ubuntu (22.04/24.04)
- Rocky Linux (9)

Requirements
------------

- Ansible 2.15 or newer

Role Variables
--------------

Defaults from `defaults/main.yml`:

```yaml
webmin_listen: "10000"
webmin_port: "10000"
webmin_ssl: "1"
webmin_reverse_proxy_referer: ""
```

- `webmin_listen`: Webmin listen socket value in `miniserv.conf`.
- `webmin_port`: Webmin TCP port.
- `webmin_ssl`: `1` to enable TLS, `0` to disable.
- `webmin_reverse_proxy_referer`: optional trusted reverse-proxy referer.

Example Playbook
----------------

```yaml
- hosts: all
  become: true
  roles:
    - role: bsmeding.webmin
      vars:
        webmin_port: "10000"
        webmin_ssl: "1"
```

Notes
-----

- Debian/Ubuntu install uses the official Webmin `newkey` APT repository.
- Rocky Linux install uses the official Webmin YUM repository.
