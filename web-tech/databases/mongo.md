# Mongo

# System
- Ubuntu 16.04

# Dependencies
this version has been compiled with SSL enabled and dynamically linked.
This requires that SSL libraries be installed seperately.

## Installation

```
# Download the latest version(3.2.9), in this case we use for Ubuntu-Linux 16.04
$ sudo wget https://fastdl.mongodb.org/linux/mongodb-linux-x86_64-ubuntu1604-3.2.9.tgz
$ sudo tar -zxvf mongodb-linux-x86_64-ubuntu1604-3.2.9.tgz
$ sudo mkdir -p /usr/local/mongodb
$ sudo cp -R -n mongodb-linux-x86_64-ubuntu1604-3.2.9/ /usr/local/mongodb/
```

### Add path to Enviroment
>
  MONGO_HOME=/usr/local/mongodb/mongodb-linux-x86_64-ubuntu1604-3.2.9
  PATH=$PATH:$MONGO_HOME/bin

### Create data directory
```
$ sudo mkdir /data/db
```

> note: Open port *27017* on iptables of security group of your vps 

## To Use

Run the server
```
$ ./usr/local/mongodb/mongodb-linux-x86_64-ubuntu1604-3.2.9/mongod
```

Open a new window in your terminal and run the mongo client
```
$ mongo
```

## Crete user / remote
```
$ ./mongo
> use cool_db

> db.createUser({
    user: 'test',
    pwd: 'secret',
    roles: [{ role: 'readWrite', db:'world'}]
})
```
## MongoDB Instance on a Remote Host
Open your client mongod
```
./mongo someurl.mongodomain.com:27017/world -u test -p secret
```

[read more on install](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-linux/)
