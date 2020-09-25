# Do non-electrical tests and upload the results to LocalDB

The GUI tool is prepared to upload QC test results to LocalDB.<br>
<br>
Please follow the link below.<br>
[QCHelper](https://gitlab.cern.ch/atlas-itk/sw/db/pixels/qc-viz-tools-dev/qc-helper/-/tree/master)

## I. Installation

Install SW in your machine.<br>
<br>
Environmental <br>
```
pip3 install PyQt5
pip3 install opencv-python (for macOS)
pip3 install opencv-python==4.1.2.30 (for macOS)
```
<br>
Install<br>
```
mkdir Workdir
cd ./Workdir    
git clone -b [latest tag] --recursive https://gitlab.cern.ch/atlas-itk/sw/db/pixels/qc-viz-tools-dev/qc-helper.git
```

## II. Run GUI
```
cd Workdir/qc-helper
python3 main.py
```
