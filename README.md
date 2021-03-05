# Run ngrok through docker

ngrok has stopped releasing its source code since version 2.0.
If you don't trust its secret code, you have the option to run
it inside a docker container. This script helps you doing just
that.

## Usage

```
ngrok-tunnel PORT
```

## Firewall

For this script to work, you have to allow connections from docker
to the port you want to use.

For example, with ufw:

```
ufw allow in on docker0 to any port $1 proto tcp
```

## Author

This script was written by André Kugland.
