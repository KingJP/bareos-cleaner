# bareos-cleaner [![Codacy Badge](https://api.codacy.com/project/badge/Grade/b1934fc24bc34251aa437ef095a8109f)](https://www.codacy.com/app/KingJP/bareos-cleaner?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=KingJP/bareos-cleaner&amp;utm_campaign=Badge_Grade)

BASH tools cleaning up Bareos database and file storage.


## Configuration

```
POOLDIR
    Directory where pool files are placed on hard drive.
    In Default setup you can find the directory in file /etc/bareos/bareos-sd.d/device/FileStorage.conf
        
MYSQL_USER
    Username for MySQL Connection
        
MYSQL_PASSWORD
    Password for MySQL Connection
```

## Commands:

```
-e
    delete empty (JobBytes=0) jobs
-p
    prune all volumes
-t
    update all volumes to "actiononpurge=Truncate"
-n
    update all volumes to "actiononpurge=None"
-Dc
    delete all jobs that have a copy job
-Do
    delete obsolete volume files from the disk (those not listed in catalog)
    NOTE: this operation can take several minutes to complete
-Dp
    delete all purged volumes from Bacula catalog
-h
    print this screen
```
