# Magento2 Docker Develop Install

This repository is dedicated to magento 2.3-develop for bug fixes and make features.

----

##### Dependencies

1) Install [docker](https://docs.docker.com/install/)
1) Install [docker-compose](https://docs.docker.com/compose/install/)
1) Install [make](https://www.gnu.org/software/make/)
1) Configure execute docker non-root 
```
sudo usermod -aG docker [your-user]
```

##### Important

Stop all docker containers or native services on uses ports 80, 443, 3306.

----

### Install

```
$ git clone git@github.com:mahsn/magento2-docker-development.git
$ cd magento2-docker-development
$ make install
```

----

### Store and admin

- Storefront: http://localdev.magento23.com 
- Admin: http://localdev.magento23.com/admin
- Username: `admin`
- Password: `123123q`

### Datasource

- PHPMyAdmin: http://localhost:8080
- Host: `magento2-database` or get IP executing `docker exec -it magento2-database bash -c "hostname -i"`
- Username: root
- Password: root


### Console PHP + Composer + NPM

```
$ make console
```

### Up Docker

```
$ make up
```

### Down Docker

```
$ make down
```

### Simple data

```
$ make simple-data
```


### About images

- [Docker MySQL](https://hub.docker.com/_/mysql)
- [Docker PHPMyAdmin](https://hub.docker.com/r/phpmyadmin/phpmyadmin)
- [Docker Nginx](https://hub.docker.com/_/nginx)
- [Docker PHP 7.2.20-alpine](https://github.com/00F100/magento-php/tree/master/alpine/7.2.20/fpm)

----