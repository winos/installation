# NODEJS

## dependencies

```
$ sudo apt-get install xz-utils
```
## installation instructions

Check your  architecture of your server with:
```
$ getconf LONG_BIT
64
$ uname -p
x86_64
```

download the stable version in this case we will download node for Linux (x64)
```
$ wget https://nodejs.org/dist/v4.4.4/node-v4.4.4-linux-x64.tar.xz
$ tar -C /usr/local --strip-components 1 -xJf node-v4.4.4-linux.x64.tar.xz
```

## Check your installation

```
$ ls -l /usr/local/bin/node
$ node -v
```

[read more](http://www.hostingadvice.com/how-to/install-nodejs-ubuntu-14-04/)
