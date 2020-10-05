# QC Software doc

This is a documentation about the SW packages for module QC.<br>
The doc describes how to use the packages according the flow of the module QC.<br>

## SW Installation and Setting up

![SW_structure](images/SW_structure.png)
* `Production DB`: A central DB for ITk,setup in Czech.<br>
* `LocalDB`: A local DB based on mongoDB to manage module info, QC results and related information.<br>
* `InfluxDB`: A DB dedicated for time series data. We use this DB to store DCS data in the QC. <br>
* `QC helper`: A SW to manage QC results, especially for non-electrical tests.<br>
* `YARR`: A SW to use electrical tests and upload the results to LocalDB.<br>
* `LabRemote`: A SW to control DCS and upload the data to LocalDB via InfluxDB. This SW is officially supported in the system but you can also use other SW in the module QC.<br>
* `Scan Operator`: A SW to use in electrical tests. It can help the user to perform the tests with YARR and LabRemote (or any other DCS controller).<br>


### I. Install DB packages and Setup the system in your DB server
[&rarr; Go to the page](setup_database.md)

### II. Install SW packages for DAQ(YARR, LabRemote, Scan Operator, QC helper) in your DAQ machine
[&rarr; Go to the page](sw_installation.md)

<br><br>
## QC flow
![Stage_and_SW](images/Stage_and_SW.png)

From the side of SW packages, the QC flow is roughly devided into two parts, bare module QC and module QC, as you can see in the figure.<br>
For bare module, we use "QC helper" to manage the QC results and upload the data to the production DB.<br>
For module QC, we use LocalDB to manage the QC results. Uploading QC results to the LocalDB is supported some DAQ SW packages. Uploading/Downloading the results to/from the production DB is supported in the LocalDB function. <br>

Please follow the QC steps from the link below.<br>

### Flow for Bare module QC
[&rarr; Go to the page](bare_module_QC_flow.md)

### Flow for module QC
[&rarr; Go to the page](module_QC_flow.md)

<br><br>
## Git repositry and corresponding version for each SW package
|SW |Git|branch|
|:-:|:-:|:-:|
|localdb-tools|[ldbtoolv1.4](https://gitlab.cern.ch/YARR/localdb-tools/-/tree/ldbtoolv1.4)|master|
|QC helper| [v1.0.0](https://gitlab.cern.ch/atlas-itk/sw/db/pixels/qc-viz-tools-dev/qc-helper/-/tree/v1.0.0) | master |
|Scan Operator |[v0.9.0](https://gitlab.cern.ch/YARR/utilities/scan-operator/-/commit/6746623b51e93fbc9b8223ff2deb8576cd49df31)  |master |
|YARR |[c629825b](https://gitlab.cern.ch/YARR/YARR/-/commit/c629825b9cd5a3f08e99f2574bcfd4ef946da3e1)  |devel|
|labRemote  | [24e7a55b](https://gitlab.cern.ch/berkeleylab/labRemote/-/commit/24e7a55b5e943db7fb6c6252c610b40d9eb8cf62)  | master |


<br><br>
## Reference
1. Document of "Traveling module"[(https://moduledaqdb.readthedocs.io/en/latest/)](https://moduledaqdb.readthedocs.io/en/latest/)
2. Yarr docs[(http://yarr.web.cern.ch/yarr/)](http://yarr.web.cern.ch/yarr/)
3. LocalDB docs[(https://localdb-docs.readthedocs.io/en/master/)](https://localdb-docs.readthedocs.io/en/master/)
4. Tutorial page for ITk production DB[(https://gitlab.cern.ch/jpearkes/itkpd_tutorial/blob/master/README.md)](https://gitlab.cern.ch/jpearkes/itkpd_tutorial/blob/master/README.md)
5. Documents for QC tutorial in February[https://qc-demonstration.readthedocs.io/en/latest/database_demonstration_flow/](https://qc-demonstration.readthedocs.io/en/latest/database_demonstration_flow/)
6. Serial Number Specification for ITk pixel modules[https://cds.cern.ch/record/2728364/](https://cds.cern.ch/record/2728364/)
7. MongoDB web[(https://www.mongodb.com)](https://www.mongodb.com)
8. InfluxDB web[(https://www.influxdata.com)](https://www.influxdata.com)
9. Gragfana web[(https://grafana.com)](https://grafana.com)

