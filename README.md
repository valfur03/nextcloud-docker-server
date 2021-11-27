# Nextcloud Docker Server

My Nextcloud server configuration

## Configuration

You need to create three files for the server to work properly:

- `mysql_password.txt`: The password of the MySQL `nextcloud` user.
- `mysql_root_password.txt`: The password of the MySQL `root` user.
- `host.env`: The domains configuration (`host.env.sample`).

### host.env

Both parameters (`VIRTUAL_HOST` and `LETSENCRYPT_HOST`) must bet set to the (sub)domain of your host in most cases.

### CAA DNS record

For the certificate to be generated, you have to configure the [CAA DNS record](https://letsencrypt.org/docs/caa).

## Installation

Then, just launch the server with:

```sh
docker-compose up
docker-compose up -d # daemon
```
