# Nginx

## Dependencies
Install the [nginx signing.key](http://nginx.org/keys/nginx_signing.key)
```
$ sudo apt-key add nginx_signing.key
```

## Installation instructions

For Debian replace codename with Debian distribution codename, and append the following to the end of the /etc/apt/sources.list file:

```
$ deb http://nginx.org/packages/ubuntu/ codename nginx
$ deb-src http://nginx.org/packages/ubuntu/ codename nginx
```

> Note: the codename for our purpose is: "xenial" [view more](http://nginx.org/en/linux_packages.html#distributions)


```
$ apt-get update
$ apt-get install nginx
```

[read more](http://nginx.org/en/linux_packages.html#stable)
