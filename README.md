# PHP Development Box with Ansible 

This is generalised PHP development box configured with a very loose
Ansible Script. 

## Usage
Change these values at the bottom of laravel.yml to reflect the correct values for your environment. 

````
  vars:
    mysqlservice: mysqld
    mysql_port: 3306
    dbuser: root
    dbname: my_big_db
    upassword: superpa55word
    domain: dev.dev
````

## TODO

* write better docs
* fix errors on up
