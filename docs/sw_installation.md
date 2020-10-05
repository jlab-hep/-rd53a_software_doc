# Install SW packages for DAQ(YARR, LabRemote, Scan Operator, QC helper) in your DAQ machine

## I. Install Yarr SW

### (i) Installation
Please follow the link bellow to install Yarr-SW.<br>
[Yarr installation](http://yarr.web.cern.ch/yarr/install/)<br>

Please use devel-localdb branch until the master branch is updated.<br>

### (ii) Setting the configuration of LocalDB
Please follow the link below to set the configuration of LocalDB for Yarr SW.<br>
[https://localdb-docs.readthedocs.io/en/1.4/script/setup-db/](https://localdb-docs.readthedocs.io/en/1.4/script/setup-db/)

## II. Install Lab Remote<br>
You can find the instructions to install labRemote on [their repo's README file](https://gitlab.cern.ch/berkeleylab/labRemote)

## III. Install Scan Operator<br>

Just clonning the code is enough. No need to build anything.
```
git clone --recursive https://gitlab.cern.ch/YARR/utilities/scan-operator.git
```

You can find a complete tutorial on how to use the Scan Operator on [their repo's README file](https://gitlab.cern.ch/YARR/utilities/scan-operator/).

## IV. Install QC helper
The GUI tool is prepared to upload QC test results to LocalDB.<br>
<br>
Please follow the link below.<br>
[QCHelper](https://gitlab.cern.ch/atlas-itk/sw/db/pixels/qc-viz-tools-dev/qc-helper/-/tree/master)
<br>
### (i). Environment
Suported OS<br>
* Cent OS 7<br>
* macOS 10.15.3<br>

Required packages<br>
* Python3<br>
* PyQt5<br>
* OpenCV<br>
Setup<br>
```
pip3 install PyQt5
pip3 install opencv-python (for macOS)
pip3 install opencv-python==4.1.2.30 (for macOS)
```
### (ii). Installation
Install QCHelper in your machine.<br>
<br>
Install<br>
```bash
mkdir Workdir
cd ./Workdir
git clone -b [latest version] --recursive https://gitlab.cern.ch/atlas-itk/sw/db/pixels/qc-viz-tools-dev/qc-helper.git
```

<br>
[&rarr; Back to the page](https://rd53a-software-docs.readthedocs.io/en/latest/rd53a_demo_flow/)
