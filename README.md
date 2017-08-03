# CodeIgniter 3 Tutorial

## Run

```console
# Run MariaDB.
$ docker run -d -p 3366:3306 -e MYSQL_ALLOW_EMPTY_PASSWORD=yes --name maria mariadb:10

# Please repeat until you succeed.
$ mysqladmin ping -h 127.0.0.1 -P 3366 -u root
mysqld is alive

# Run ddl.sql.
$ mysql -h 127.0.0.1 -P 3366 -u root < misc/sql/ddl.sql

# Run application.
$ docker run -d -p 8080:80 -v $(pwd):/var/www --link maria --name ci3-tutorial 178inaba/php7-nginx
```

---

# What is CodeIgniter

CodeIgniter is an Application Development Framework - a toolkit - for people
who build web sites using PHP. Its goal is to enable you to develop projects
much faster than you could if you were writing code from scratch, by providing
a rich set of libraries for commonly needed tasks, as well as a simple
interface and logical structure to access these libraries. CodeIgniter lets
you creatively focus on your project by minimizing the amount of code needed
for a given task.

## Release Information

This repo contains in-development code for future releases. To download the
latest stable release please visit the [CodeIgniter Downloads](https://codeigniter.com/download) page.

## Changelog and New Features

You can find a list of all changes for each release in the 
[user guide change log](https://github.com/bcit-ci/CodeIgniter/blob/develop/user_guide_src/source/changelog.rst).

## Server Requirements

PHP version 5.6 or newer is recommended.

It should work on 5.3.7 as well, but we strongly advise you NOT to run
such old versions of PHP, because of potential security and performance
issues, as well as missing features.

## Installation

Please see the [installation section](https://codeigniter.com/user_guide/installation/index.html)
of the CodeIgniter User Guide.

## License

Please see the [license agreement](https://github.com/bcit-ci/CodeIgniter/blob/develop/user_guide_src/source/license.rst).

## Resources

-  [User Guide](https://codeigniter.com/docs)
-  [Language File Translations](https://github.com/bcit-ci/codeigniter3-translations)
-  [Community Forums](http://forum.codeigniter.com/)
-  [Community Wiki](https://github.com/bcit-ci/CodeIgniter/wiki)
-  [Community IRC](https://webchat.freenode.net/?channels=%23codeigniter)

Report security issues to our [Security Panel](mailto:security@codeigniter.com)
or via our [page on HackerOne](https://hackerone.com/codeigniter), thank you.

## Acknowledgement

The CodeIgniter team would like to thank EllisLab, all the
contributors to the CodeIgniter project and you, the CodeIgniter user.
