# Do electrical tests and upload the results to LocalDB

## I. Set and Run scans 
### (i) Login mongoDB
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

### (ii) Settings for Scan Operator and Run scans

The Scan Operator configuration is based on json files. All the available options and settings are described on the "Basic configuration" section of their [README file](https://gitlab.cern.ch/YARR/utilities/scan-operator).

## II. Monitor DCS in Grafana

Please refer to the following page used in the tutorial on February.<br>
[https://qc-demonstration.readthedocs.io/en/latest/database_demonstration_grafana/](https://qc-demonstration.readthedocs.io/en/latest/database_demonstration_grafana/)<br>

## III. Check the results in LocalDB viewer
Open your browser and access the LocalDB viewer.<br>
The url is [http://127.0.0.1:5000/localdb](http://127.0.0.1:5000/localdb) or https://IPADRESS:5000/localdb.<br><br>

Go to the module's toppage following the instruction below.<br>
![Go_to_Module_Toppage](images/goto_module_toppage.png)<br>

You can see the uploaded scan results in the table of "Scan Data" in the page as below.<br>
You can go to the result page for each test by clicking the ids in the table.<br>
![View_QC_Test](images/view_scans.png)<br>


## IV. Select scan results as QC results in LocalDB viewer
[Select_Scan_Result](select_scans.md)

<br>
[&rarr; Back to the page](module_QC_flow.md)
