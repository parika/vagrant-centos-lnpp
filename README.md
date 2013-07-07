# vagrant-centos64-lnpp

**LNPP** - **l**inux, **n**ginx, **p**ercona(-server), **p**hp(-fpm)

## What's in the box?
Given box is built on CentOS 6.4 x86_64 minimal - [read more](http://wiki.centos.org/Manuals/ReleaseNotes/CentOSMinimalCD6.4)

Additional packages:
 * [nginx](http://nginx.org/) 1.4.1
 * [php](http://www.php.net/) 5.4.17
  * fpm
  * mbstring
  * xml
  * pdo
  * mysql
  * intl
  * xdebug 2.2.3 (pecl)
  * apc 3.1.15 (pecl)
  * memcache 3.0.8 (pecl)
  * redis 2.2.3 (pecl)
 * [percona-server](http://www.percona.com/software/percona-server) 5.5.31
 * [memcached](http://memcached.org/) 1.4.15
 * [redis](http://redis.io/) 2.6.13

Box last updated: 07.07.2013

### Vagrantfile
Vagrantfile contains following information:
 * port forwarding from host 8080 to quest 80
 * port forwarding from host 8181 to quest 8080
 * port forwarding from host 3306 to quest 3306
 * nfs mount from host ../srv to quest /srv
 * nginx restart (as additional nginx conf will be included from mounted nfs folder)

Box will automatically be downloaded from [Dropbox](https://dl.dropbox.com/s/6r4t3grdnhoavb9/CentOS-6.4-lnpp.box).

### Usage:

 1. Download as Zip
 2. Extract
 3. cd to dir
 4. execute "vagrant up"
