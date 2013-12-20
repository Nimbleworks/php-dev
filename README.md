# PHP Development Box with Ansible 

This is generalised PHP development box configured with a very loose
Ansible Script. 

## Usage
Change these values at the bottom of laravel.yml to reflect the correct values for your environment. 

It contains the following LAMP setup: 

* latest php (5.5 at time of press)
* MySQL
* Sqlite
* Apache
* php5-gd
* php5-mcrypt
* php5-curl

You also get: 

* vim 
* SASS (via Ruby and the Gem)
* the wonders of Ubuntu.
* node.js
* Grunt


````
  vars:
    mysqlservice: mysqld
    mysql_port: 3306
    dbuser: root
    dbname: my_big_db
    upassword: superpa55word
    domain: dev.dev
````

## Setup 
To create the site directory (this will become the contents of the /var/www/ folder)

````
ln -s ~/site/directory ./site
````

## TODO

* write better docs
* fix errors on up
