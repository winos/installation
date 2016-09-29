# Nginx

**version:** 1.10.0

## Dependencies
Install the [nginx signing.key](http://nginx.org/keys/nginx_signing.key)
```
$ sudo apt-key add nginx_signing.key
```

## Installation instructions

For Ubuntu replace codename with Ubuntu distribution codename, and append the following to the end of the /etc/apt/sources.list file:

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


## Compile from source
1. Download the source code
2. Configure: 

```
$ cd nginx
$ ./auto/configure  \
   --user=nginx     \
   --group=nginx    \
   --prefix=/etc/nginx  \
   --sbin-path=/usr/sbin/nginx  \
   --conf-path=/etc/nginx/nginx.conf  \
   --pid-path=/var/run/nginx.pid  \
   --lock-path=/var/run/nginx.lock  \
   --error-log-path=/var/log/nginx/error.log  \
   --http-log-path=/var/log/nginx/access.log  \
   --with-http_gzip_static_module      \
   --with-http_stub_status_module    \
   --with-http_ssl_module      \
   --with-pcre  \
   --with-http_realip_module   \
   --without-http_scgi_module   \ 
   --without-http_uwsgi_module   \
   --without-http_fastcgi_module
$ make
$ sudo make install 
```
[about configuration](http://nginx.org/en/docs/configure.html)

## Problem solving
**403 Forbidden**

Set 755 permissions from your FTP client to the affected directory.
```
$ chmod 755 /path/of/your/directory/ -v
// or if the issue is for any file:
$ chmod 644 /path/of/your/directory/filename.ext -v

 ```
[read more](https://www.scalescale.com/tips/nginx/403-forbidden-nginx/)
