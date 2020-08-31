# RD53A Demonstration doc

This is a documentation about the SW packages for module QC.<br>
The doc describes how to use the packages folloing the flow of the module assembly and its QC.<br>

![SW_structure](images/SW_structure.png)
* `Production DB`: A central DB for ITk,setup in Czech.
* `LocaalDB`: A local DB based on mongoDB to store module info, scan results and so on.
* `InfluxDB`: A DB dedicated for time series data to store DCS data. 
* `QC helper`: A SW to register QC results to LocalDB, especially for Non-electrical tests.
* `YARR`: A SW to use electrical tests and upload the results to LocalDB.
* `LabRemote`: A SW to control DCS and upload the data to LocalDB via InfluxDB.
* `Scan Operator`: A SW to use in electrical tests. It can help the user operation in the tests with YARR and LabRemote.

![Stage_and_SW](images/Stage_and_SW.png)

In the flow of the module assembly, we recept a bare module and PCB.<br>
In the first step of the flow,we need to do QC tests for the bare module. We use "QC helper"

**Flow for Bare module QC**
* [bare_module_QC_flow](bare_module_QC_flow.md)

**Flow for module(bare + flex) QC**
* [module_QC_flow](module_QC_flow.md)

## Reference
1. Document of "Traveling module"[(https://moduledaqdb.readthedocs.io/en/latest/)](https://moduledaqdb.readthedocs.io/en/latest/)
2. Yarr docs[(https://yarr.readthedocs.io/en/latest/)](https://yarr.readthedocs.io/en/latest/)
3. LocalDB docs[(https://localdb-docs.readthedocs.io/en/master/)](https://localdb-docs.readthedocs.io/en/master/)
4. Tutorial page for ITk production DB[(https://gitlab.cern.ch/jpearkes/itkpd_tutorial/blob/master/README.md)](https://gitlab.cern.ch/jpearkes/itkpd_tutorial/blob/master/README.md)
5. Documents for QC tutorial in February[]()
6. Module QC documentation[(https://cds.cern.ch/record/2702738/files/ATL-COM-ITK-2019-045.pdf?)](https://cds.cern.ch/record/2702738/files/ATL-COM-ITK-2019-045.pdf?)
7. MongoDB web[(https://www.mongodb.com)](https://www.mongodb.com)
8. InfluxDB web[(https://www.influxdata.com)](https://www.influxdata.com)
9. Gragfana web[(https://grafana.com)](https://grafana.com)

## Contact

* Please send questions or comments to: hiroki.okuyama at cern.ch
* Also a dedicated mattermost channel:[https://mattermost.web.cern.ch/yarr/channels/qc-demonstration](https://mattermost.web.cern.ch/yarr/channels/qc-demonstration)

