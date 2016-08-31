# Mongo

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


## To Use

Run the server
```
$ mongod
```

Open a new window in your terminal and run the mongo client
```
$ mongo
```

[read more on install](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-linux/)
