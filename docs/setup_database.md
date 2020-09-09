The following manual has to be executed by Admin in your site.
# Installation
Refer to the following page in LocalDB docs:<br>
[https://localdb-docs.readthedocs.io/en/devel-localdb/installation/](https://localdb-docs.readthedocs.io/en/devel-localdb/installation/)

#I. Setting for mongo DB

##1. Create an account in mongoDB as admin<br>
Refer to the following page in LocalDB docs:<br>
[https://localdb-docs.readthedocs.io/en/devel-localdb/script/create_admin/](https://localdb-docs.readthedocs.io/en/devel-localdb/script/create_admin/)

##2. Lock mongoDB
Lock the mongoDB so that only those who know the account name and password can read and write to it.<br>
Follow the commands below:


Stop MongoDB instance:

```bash
$ sudo systemctl stop mongod.service
```

Enable or uncomment out security.authorization in /etc/mongod.conf:

```yml
...
security:
    authorization: enabled
...
```

Start MongoDB instance:

```bash
$ sudo systemctl start mongod.service
```

#II. Launch LocalDB viewer
Create config file to setup viewer and Start LocalDB viewer following the page below:<br>
[https://localdb-docs.readthedocs.io/en/devel-localdb/script/setup-viewer/](https://localdb-docs.readthedocs.io/en/devel-localdb/script/setup-viewer/)
<br>
<span style="color: red; ">**We can see the viewer while the process is running.**</span><br>


#II. Setting for LocalDB

## 1. Check the mail function

## 2. Download institution info from the production DB

## 3. Register QC user in LocalDB viewer 
