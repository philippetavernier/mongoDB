# mongoDB

phil@phil-OptiPlex-790:~$ cat /etc/mongod.conf 
# mongod.conf

# for documentation of all options, see:
#   http://docs.mongodb.org/manual/reference/configuration-options/

# Where and how to store data.
storage:
  dbPath: /var/lib/mongodb
  journal:
    enabled: true
#  engine:
#  mmapv1:
#  wiredTiger:

# where to write logging data.
systemLog:
  destination: file
  logAppend: true
  path: /var/log/mongodb/mongod.log

# network interfaces
net:
  port: 27017
  bindIp: 127.0.0.1


# how the process runs
processManagement:
  timeZoneInfo: /usr/share/zoneinfo

#security:

#operationProfiling:

#replication:

#sharding:

## Enterprise-Only Options:

#auditLog:

#snmp:


phil@phil-OptiPlex-790:~$ ls /var/lib/mongodb
collection-0--878691929929129107.wt  journal
collection-2--878691929929129107.wt  _mdb_catalog.wt
collection-4--878691929929129107.wt  mongod.lock
collection-7--878691929929129107.wt  sizeStorer.wt
diagnostic.data                      storage.bson
index-1--878691929929129107.wt       WiredTiger
index-3--878691929929129107.wt       WiredTigerHS.wt
index-5--878691929929129107.wt       WiredTiger.lock
index-6--878691929929129107.wt       WiredTiger.turtle
index-8--878691929929129107.wt       WiredTiger.wt
index-9--878691929929129107.wt

You can run mongo shell without any command-line options to connect to a MongoDB instance running on your localhost with default port 27017:

https://docs.mongodb.com/manual/mongo/



