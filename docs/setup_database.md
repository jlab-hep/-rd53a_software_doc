The following manual has to be executed by Admin in your site.
## Installation
Refer to the following page in LocalDB docs:<br>
Installation for your DB machine[(https://localdb-docs.readthedocs.io/en/devel-localdb/installation/)](https://localdb-docs.readthedocs.io/en/devel-localdb/installation/)

## Setting for mongo DB
###Create an account in mongoDB as admin refering the following page:<br>
Create Admin for LocalDB[(https://localdb-docs.readthedocs.io/en/devel-localdb/script/create_admin/)](https://localdb-docs.readthedocs.io/en/devel-localdb/script/create_admin/)

###Lock mongoDB
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

## Setting for LocalDB viewer
Create config file to setup viewer and Start LocalDB viewer following the page below:<br>
Setup Viewer [(https://localdb-docs.readthedocs.io/en/devel-localdb/script/setup-viewer/)](https://localdb-docs.readthedocs.io/en/devel-localdb/script/setup-viewer/)
<span style="color: red; ">**We can see the viewer while the process is running.**</span><br>

## Check the mail function

## Download institution info from the production DB

## Register QC user in LocalDB viewer 
