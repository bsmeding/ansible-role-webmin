Ansible Role for Webmin
=======================

Ansible Role for Webmin Installation.

Two variables that can be set:
Listen port
webmin_port: "10000"

# Set SSL enabled?  Webmin use 1 for true and 0 for false in config
webmin_ssl: "1"

# Use reverse proxy?
When using reverse proxy, the Trusted Reverers must be set. This can be done by the GUI, but also set in config directly. For example you can set webmin.doman.tld from your reverse proxy to http://webmin.server:10000 you need to set this referer URL here:

webmin_reverse_proxy_referer: ''


Requirements
------------

This role require/tested on Ansible 2.2 or higher.

Used for Ubuntu and Debian based distribution

Tested on
---------



