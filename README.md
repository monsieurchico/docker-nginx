# Nginx image

## Requirements

You must have [Docker](https://www.docker.com/) >= 1.5.

## What's inside

* [latest ubuntu](https://github.com/dockerfile/ubuntu)
* [latest development nginx](http://nginx.org/en/download.html)

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
  -d \
  --name nginx \
  -p 80:80 \
  -p 443:443 \
  -v /opt/docker/nginx/vhost:/etc/nginx/sites-enabled \
  -v /opt/docker/nginx/logs:/var/log/nginx \
  -v /opt/docker/nginx/code:/var/www \
   monsieurchico/nginx
```
