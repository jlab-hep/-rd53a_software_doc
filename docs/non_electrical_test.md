# Do non-electrical tests and upload the results to LocalDB

The GUI tool is prepared to upload QC test results to LocalDB.<br>
<br>
Please follow the link below.<br>
[QCHelper](https://gitlab.cern.ch/atlas-itk/sw/db/pixels/qc-viz-tools-dev/qc-helper/-/tree/master)
<br>
## I. Environment
Suported OS
* Cent OS 7
* macOS 10.15.3

Required packages
*  Python3
*  PyQt5
*  OpenCV

Setup<br>
<br>
```
pip3 install PyQt5
pip3 install opencv-python (for macOS)
pip3 install opencv-python==4.1.2.30 (for macOS)
```
<br>
## II. Installation
Install QCHelper in your machine.<br>
<br>
Install<br>
```
mkdir Workdir
cd ./Workdir
git clone -b [latest version] --recursive https://gitlab.cern.ch/atlas-itk/sw/db/pixels/qc-viz-tools-dev/qc-helper.git
```
<br>
## III. Run GUI
```
cd Workdir/qc-helper
python3 main.py
```
