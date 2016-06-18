Ansible role - courier-imap installer
=====

[![Build Status](https://travis-ci.org/repleo/ansible-role-courier-imap.svg?branch=master)](https://travis-ci.org/repleo/ansible-role-courier-imap)
[![Ansible Galaxy](http://img.shields.io/badge/galaxy-repleo.courier-imap-660198.svg?style=flat)](https://galaxy.ansible.com/repleo/courier-imap)

This role install and configures courier-imap suite. Courier-imap comes with courier-imap-ssl, salsauthd for smtp authentication and maildrop for mail delivery

Requirements
------------

This role requires Ansible 2.0 or higher and platform requirements are listed in the metadata file.

Role Variables
--------------

   # SSL Configuration.
   courier-imap_ssl: yes
   courier-imap_ssl_certificate: "/etc/nginx/ssl/courier-imap.crt"
   courier-imap_ssl_certificate_key: "/etc/nginx/ssl/courier-imap.key"

To disable SSL, just import the role without variables.

Dependencies
------------

None

Example Playbook
----------------

Install courier-imap
```yaml
- { role: repleo.courier-imap,
     courier_ssl: yes,
     courier_ssl_certificate: /etc/courier/imap.repleo.nl-chain.pem,
     courier_ssl_certificate_key: /etc/courier/imap.repleo.nl.key
  }
```

License
-------

GPL v3 - (c) 2016, Repleo, Amstelveen

Author Information
------------------

Repleo, Amstelveen, Holland -- www.repleo.nl  
Jeroen Arnoldus (jeroen@repleo.nl)


