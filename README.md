# Nginx image

Nginx image.

## Requirements

You must have [Docker](https://www.docker.com/) installed.

## What's inside

* (latest ubuntu)[https://github.com/dockerfile/ubuntu]
* (latest development nginx)[http://nginx.org/en/download.html]

### Ports

You can bind ports :

* 80
* 443

### Volumes

You can mount directories :

* /etc/nginx/sites-enabled : virtual hosts
* /etc/nginx/certs : certificates
* /etc/nginx/conf.d : extra configuration files
* /var/log/nginx : logs
* /var/www : code

## Usage

```bash
# pull (auto) and run
docker run \
  -d monsieurchico/nginx \
  -t nginx

# expose ports
docker run \
  -d monsieurchico/nginx \
  -t nginx \
  -p 80:80 \
  -p 443:443

# mount volumes
docker run \
  -d monsieurchico/nginx \
  -t nginx \
  -p 80:80 \
  -p 443:443 \
  -v /path/to/my/vhost:/etc/nginx/sites-enabled
  -v /path/to/my/logs:/var/log/nginx
  -v /path/to/my/code:/var/www
```
