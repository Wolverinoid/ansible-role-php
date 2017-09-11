Ansible Role PHP
=========

Ansible role allows to manage php on ubuntu / debian server


Role Variables
--------------
```yaml
---
# PHP Default parameters
php_version: 5.6
php_extensions:
- php-all-dev
- php-amqp
- php-apcu
- php-apcu-bc
- php-gearman
- php-geoip
- php-gmagick
- php-gnupg
- php-http
- php-igbinary
- php-imagick
- php-libsodium
- php-mailparse
- php-memcache
- php-memcached
- php-mongodb
- php-msgpack
- php-oauth
- php-phalcon
- php-propro
- php-radius
- php-raphf
- php-redis
- php-rrd
- php-solr
- php-ssh2
- php-tideways
- php-uuid
- php-xdebug
- php-yac
- php-yaml
- php-zmq
php_modules: 
- php7.1-bcmath
- php7.1-bz2
- php7.1-cgi
- php7.1-cli
- php7.1-common
- php7.1-curl
- php7.1-dba
- php7.1-dev
- php7.1-enchant
- php7.1-gd
- php7.1-gmp
- php7.1-imap
- php7.1-interbase
- php7.1-intl
- php7.1-json
- php7.1-ldap
- php7.1-mbstring
- php7.1-mcrypt
- php7.1-mysql
- php7.1-odbc
- php7.1-opcache
- php7.1-pgsql
- php7.1-phpdbg
- php7.1-pspell
- php7.1-readline
- php7.1-recode
- php7.1-snmp
- php7.1-soap
- php7.1-sqlite3
- php7.1-sybase
- php7.1-tidy
- php7.1-xml
- php7.1-xmlrpc
- php7.1-xsl
- php7.1-zip


# PHP-FPM parameters
php_fpm: false
php_fpm_pool_config_path: /etc/php5/fpm/pool.d/www.conf
php_fpm_pool_user: www-data
php_fpm_pool_group: www-data
php_fpm_listen: /var/run/php5-fpm.sock
php_fpm_pm_max_children: 5
php_fpm_daemon: php5-fpm
php_fpm_ini_path: /etc/php5/fpm/php.ini

php_composer_path: '/usr/local/bin/'
php_composer_name: 'composer'
php_composer: false
```

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  become: true
  roles:
     - { role: php, php_version: "7.1", php_modules: ['snmp', 'sqlite3'], php_extensions: ['amqp', 'mongodb'] }
```     


License
-------

Apache

Author Information
------------------

Aleksandr Ivanov (avic.ivanov@gmail.com)
