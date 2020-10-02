# Set and Run scans 

## I. Login mongoDB
Need to log in to get the authenticate for the mongo DB. You can upload the test results after the operation.<br>
Please execute the following commands to use the scripts in Yarr/localdb/ directry<br>
```bash
$ cd <YOUR_WORD_DIRECTORY>/Yarr
$ source localdb/login_mongodb.sh 
Input mongodb account username: okuyama                     
Input mongodb account password: 
[14:36:57:446][  info  ][   Local DB    ]: -----------------------
[14:36:57:449][  info  ][   Local DB    ]: Checking connection to DB Server: mongodb://127.0.0.1:27017/localdb ...
[14:36:57:501][  info  ][   Local DB    ]: ---> Good connection!
[14:36:57:615][  info  ][   Local DB    ]: -> Set user config: /Users/okuyama/.yarr/localdb/user.json
[14:36:57:615][  info  ][   Local DB    ]: ~~~ {
[14:36:57:616][  info  ][   Local DB    ]: ~~~   "userName": "okuyama"
[14:36:57:616][  info  ][   Local DB    ]: ~~~   "institution": "~~"
[14:36:57:616][  info  ][   Local DB    ]: ~~~   "description": "viewer"
[14:36:57:616][  info  ][   Local DB    ]: ~~~   "viewerUser": "okuyama"
[14:36:57:616][  info  ][   Local DB    ]: ~~~ }
[14:36:57:616][  info  ][   Local DB    ]: -> Set site config: /Users/okuyama/.yarr/localdb/HirokinoMacBook-ea.local_site.json
[14:36:57:617][  info  ][   Local DB    ]: ~~~ {
[14:36:57:617][  info  ][   Local DB    ]: ~~~ }
[14:36:57:617][  info  ][   Local DB    ]: -----------------------

[LDB] Login successful.
[LDB] Username and password are saved.
```

## II. Settings for Scan Operator

The Scan Operator configuration is based on json files. All the available options and settings are described on the "Basic configuration" section of their [README file](https://gitlab.cern.ch/YARR/utilities/scan-operator).

<br>
[&rarr; Back to the page](electrical_test.md)
