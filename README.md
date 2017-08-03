# CodeIgniter 3 Tutorial

This application is the result of CodeIgniter 3 tutorial.

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

Open http://localhost:8080/ in your browser.

## License

[MIT](LICENSE)

## Author

[178inaba](https://github.com/178inaba)
