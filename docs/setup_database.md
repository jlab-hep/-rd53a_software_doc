The following manual has to be executed by Admin in your site.
# Requirement OS
**CentOS7** is needed for this QC flow.<br>
Other requiements are described in the following page.<br>
[https://localdb-docs.readthedocs.io/en/1.4/installation/requirements-list/](https://localdb-docs.readthedocs.io/en/1.4/installation/requirements-list/)

# I. Installation
<span style="color: red; ">**Please skip this step if you have already installed LocalDB.**</span><br>
Clone localdb-tools in your working directory.<br>
```bash
$ cd <YOUR_WORK DIRECTRY>
$ git clone https://gitlab.cern.ch/YARR/localdb-tools.git
```

Refer to the following page.**YARR installation is not required if the machine is not for DAQ.**<br>
[https://localdb-docs.readthedocs.io/en/1.4/installation/manual-centos/](https://localdb-docs.readthedocs.io/en/1.4/installation/manual-centos/)

#II. Setting for mongo DB

##(i). Create an account in mongoDB as admin<br>
Refer to the following page.<br>
[https://localdb-docs.readthedocs.io/en/devel-localdb/script/create_admin/](https://localdb-docs.readthedocs.io/en/devel-localdb/script/create_admin/)<br>
**In case you already have an account in LocalDB...**<br>
Please execute this script for the same name and password as admin to up to supprt the latest system.<br>
You need to unlock mongoDB before executing the script. Refer to the next step.<br>

##(ii). Lock mongoDB
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

#III. Launch LocalDB viewer
Create config file to setup viewer and Start LocalDB viewer following the page below:<br>
[https://localdb-docs.readthedocs.io/en/1.4/script/setup-viewer/](https://localdb-docs.readthedocs.io/en/1.4/script/setup-viewer/)
<br>
<span style="color: red; ">**We can see the viewer while the process is running.**</span><br>


#IV. Setting for LocalDB
Please open your browser and access the LocalDB viewer.<br>
The url is [http://127.0.0.1:5000/localdb](http://127.0.0.1:5000/localdb) or https://IPADRESS:5000/localdb.<br><br>

Go to the admin page following the instruction below.<br>
![Go_to_Admin_Page](images/goto_adminpage.png)<br>
Please do the folloing setting.<br>

## (i). Download institution lists from the production DB
Please follow the link below.<br>
[Download_Institute](download_institution.md)

## (ii). Check the mail function
Please follow the link below.<br>
[Check_Mail](check_mail.md)

## (iii). Register QC user in LocalDB viewer 
Please follow the link below.<br>
[Create_User](create_user.md)


