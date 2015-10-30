localcloud-php
=========

This role will install latest stable php release with a configurable list of modules, expose important settings and
manage your fpm pool set up. Use this to quickly install and manage your php deployment in a reliable way.

Requirements
------------

An Ubuntu 14 LTS box.

Role Variables
--------------

All variables listed below will allow you to control your php installation. All of them are optional and will
fall back to reasonable defaults. If you need a configuration option- raise an issue and we'll add it.

PHP:

`php_manage_ini`
`php_modules`
`php_memory_limit`
`php_error_reporting`
`php_display_errors`
`php_log_errors`
`php_post_max_size`
`php_upload_max_filesize`
`php_max_file_uploads`
`php_date_timezone`
`php_fix_pathinfo`

FPM:

`php_manage_fpm_config`

DEFAULT FPM-POOL:

`php_manage_default_pool`




Dependencies
------------

This role depends on [localcloud-common](https://github.com/dmitrybelyakov/ansible-localcloud-common) role to be
in place.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:


```yml
- hosts: servers
  roles:
     - localcloud-common
     - localcloud-php

```

License
-------

BSD

License
-------

MIT License
