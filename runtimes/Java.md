# Java

## Dependencies
```
$ sudo apt-get install libc6-i386
```

## Installation instructions
1. Download the last source, go to
[Java](http://www.oracle.com/technetwork/java/javase/downloads/index.html)

```
$ mv jdk-8u91-linux-i586.tar.gz /usr/lib/jvm/ && cd /usr/lib/jvm/
$ sudo tar xvzf jdk-8u91-linux-i586.tar.gz
// it should generate a folder named jdk1.8.0_91
```

## Add to JAVA_HOME to PATH
Edit the file named "/etc/profile" and paste this code into:
```
JAVA_HOME=/usr/lib/jvm/jdk1.8.0_91
PATH=$PATH:$HOME/bin:$JAVA_HOME/bin
export JAVA_HOME
export PATH
```
> Note: Restart for changes to take effect

## Check the install
```
$ java -version
```

[read more](http://es.wikihow.com/instalar-Oracle-Java-JDK-en-Ubuntu-Linux)
