# Nextcloud Docker Server

My Nextcloud server configuration

## Configuration

You need to create two files for the server to work properly:

- `mysql_password.txt`: The password of the MySQL `nextcloud` user.
- `mysql_root_password.txt`: The password of the MySQL `root` user.

Then, just launch the server with:

```sh
docker-compose up
docker-compose up -d # daemon
```
