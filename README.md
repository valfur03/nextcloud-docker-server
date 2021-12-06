# Nextcloud Docker Server

My Nextcloud server configuration

> This Docker service is intended to run with my [NGINX proxy entrypoint](https://github.com/valfur03/nginx-proxy-entrypoint) repo.

## Configuration

You need to create three files for the server to work properly:

- `mysql_password.txt`: The password of the MySQL `nextcloud` user.
- `mysql_root_password.txt`: The password of the MySQL `root` user.
- `host.env`: The domains configuration (`host.env.sample`).

To work with the NGINX proxy entrypoint Docker service, you have to create a network called `certs`.

```sh
docker network create certs
```

### host.env

Both parameters (`VIRTUAL_HOST` and `LETSENCRYPT_HOST`) must bet set to the (sub)domain of your host in most cases.

## Installation

Then, just launch the server with:

```sh
docker-compose up
docker-compose up -d # daemon
```
