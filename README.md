localcloud-php
=========

This role will install latest stable php release with a configurable list of modules, expose important settings and
manage your fpm pool set up. Use this to quickly install and manage your php deployment and composer package manager
in a reliable way.

Requirements
------------

An Ubuntu 14 LTS box.

Role Variables
--------------

All variables listed below will allow you to control your php installation. All of them are optional and will
fall back to reasonable defaults. If you need a configuration option- raise an issue and we'll add it.

***PHP:***

`php_manage_ini`
Whether to use all the variables below and overwrite default php.ini file. Disable this to manage PHP configuration yourself manually.

`php_modules`
A list of PHP modules that should be present. Default configuration will install production ready setup. You may need to modify that depending on your build requirements.

`php_memory_limit`
Limit memory available to PHP.

`php_error_reporting`
Whether to report errors.

`php_display_errors`
And whether to display them.


`php_log_errors`
Write error messages to PHP log file.

`php_post_max_size`
Maximum allowed post size in megabytes.

`php_upload_max_filesize`
Maximum size for uploaded files in megabytes.

`php_max_file_uploads`
Maximum number of files accepted simultaneously.

`php_date_timezone`
PHP default timezone.

`php_fix_pathinfo`
Whether to fix scrip path info. This setting may be useful for some NGINX/PHP-FPM setups.



***FPM:***

`php_manage_fpm_config`
Same as with ini file - specifies whether Ansible should manage your PHP FPM configuration.
There are currently no fpm configuration options exposed. If you need to configure some settings, please raise an issue and we'll expose those settings.


DEFAULT FPM-POOL:

`php_manage_default_pool`
Same as with ini file - specifies whether Ansible should manage your default FPM pool configuration.
There are currently no fpm pool configuration options exposed. If you need to configure some settings, please raise an issue and we'll expose those settings.


Dependencies
------------

This role depends on [localcloud-common](https://github.com/dmitrybelyakov/ansible-localcloud-common) role to be
in place.

Example Playbook
----------------


```yml
- hosts: servers
  roles:
     - localcloud-common
     - localcloud-php

```


License
-------

MIT License
