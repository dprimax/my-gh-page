---
title: "Reset MySQL root Password on Ubuntu 16.04"
date: 2017-12-06
tags: ["mysql", "ubuntu", "server", "password"]
draft: false
---

1. Stop MySQL service

    `$ sudo service mysql stop`

2. Enter to MySQL safe mode

    `$ sudo mysqld_safe --skip-grant-tables --skip-networking &`

3. Login as root

    `$ mysql -u root`

4. Flush privileges

    `mysql> FLUSH PRIVILEGES;`

5. Change old forgotten password with Your desired one

    `mysql> ALTER USER 'root'@'localhost' IDENTIFIED BY ‘your_new_password';`

6. Exit from MySQL

    `mysql> exit`

7. Kill all MySQL(s) process then restart its service

    `sudo service mysql start`
