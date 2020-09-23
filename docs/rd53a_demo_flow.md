# RD53A Software doc

This is a documentation about the SW packages for module QC.<br>
The doc describes how to use the packages folloing the flow of the module assembly and its QC.<br>

![SW_structure](images/SW_structure.png)
* `Production DB`: A central DB for ITk,setup in Czech.<br>
* `LocalDB`: A local DB based on mongoDB to store module info, scan results and so on.<br>
* `InfluxDB`: A DB dedicated for time series data to store DCS data. <br>
* `QC helper`: A SW to register QC results to LocalDB, especially for Non-electrical tests.<br>
* `YARR`: A SW to use electrical tests and upload the results to LocalDB.<br>
* `LabRemote`: A SW to control DCS and upload the data to LocalDB via InfluxDB.<br>
* `Scan Operator`: A SW to use in electrical tests. It can help the user to perform the tests with YARR and LabRemote (or any other DCS controller).<br>

![Stage_and_SW](images/Stage_and_SW.png)

In the flow of the module assembly, we recept a bare module and PCB.<br>
For bare module QC, we only use "QC helper". It helps QC test and analysis results. It also interfaces to the production DB.<br>
For module QC, we use LocalDB for data management system. We store QC results to the DB and upload/download the data
to sync the production DB.<br>

Please follow the QC steps from the link below.<br>

## Flow for Bare module QC
[bare_module_QC_flow](bare_module_QC_flow.md)

## Setup LocalDB in your DB server
[setup_database](setup_database.md)

## Flow for module(bare + PCB) QC
[module_QC_flow](module_QC_flow.md)

## Git repositry and corresponding version for each SW package
|SW |Git|branch|
|:-:|:-:|:-:|
|localdb-tools|[ldbtoolv1.4](https://gitlab.cern.ch/YARR/localdb-tools/-/tree/ldbtoolv1.4)|master|
|QC helper|- |- |
|Scan Operator |[v0.9.0](https://gitlab.cern.ch/YARR/utilities/scan-operator/-/commit/6746623b51e93fbc9b8223ff2deb8576cd49df31)  |master |
|YARR |[680f0adc](https://gitlab.cern.ch/YARR/YARR/-/commit/680f0adc7d91c611e43039835f92eae7c50da830)  |devel-localdb|
|labRemote  | [24e7a55b](https://gitlab.cern.ch/berkeleylab/labRemote/-/commit/24e7a55b5e943db7fb6c6252c610b40d9eb8cf62)  | master |


## Reference
1. Document of "Traveling module"[(https://moduledaqdb.readthedocs.io/en/latest/)](https://moduledaqdb.readthedocs.io/en/latest/)
2. Yarr docs[(http://yarr.web.cern.ch/yarr/)](http://yarr.web.cern.ch/yarr/)
3. LocalDB docs[(https://localdb-docs.readthedocs.io/en/master/)](https://localdb-docs.readthedocs.io/en/master/)
4. Tutorial page for ITk production DB[(https://gitlab.cern.ch/jpearkes/itkpd_tutorial/blob/master/README.md)](https://gitlab.cern.ch/jpearkes/itkpd_tutorial/blob/master/README.md)
5. Documents for QC tutorial in February[]()
6. Module QC documentation[(https://cds.cern.ch/record/2702738/files/ATL-COM-ITK-2019-045.pdf?)](https://cds.cern.ch/record/2702738/files/ATL-COM-ITK-2019-045.pdf?)
7. MongoDB web[(https://www.mongodb.com)](https://www.mongodb.com)
8. InfluxDB web[(https://www.influxdata.com)](https://www.influxdata.com)
9. Gragfana web[(https://grafana.com)](https://grafana.com)

