localcloud-php
=========

This role will install latest stable php release with a configurable list of modules. Use this to quickly install and manage your php deployment and composer package manager in a reliable way.

Requirements
------------

An Ubuntu 18.04+ LTS box.

Role Variables
--------------

All variables listed below will allow you to control your php installation. All of them are optional and will fall back to reasonable defaults. 
***PHP:***

`php_repository` Reposity to install PHP and its extensions from. This will default to `ppa:ondrej/php`. Keep in mind that this affects module package names.

`php_service_name` The name of FPM service. This ensures the service is properly restarted.


`php_modules`
A list of PHP modules that should be present. Default configuration will install production ready setup. You may need to modify that depending on your build requirements.


Dependencies
------------

This role has no dependencies.

Example Playbook
----------------


```yml
- hosts: servers
  roles:
     - localcloud-php

```


License
-------

MIT License
