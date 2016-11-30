# KITE
## Introduction
This framework is streamlining InSAR displacement processing routines for earthquake inversion through [pyrocko](http://www.pyrocko.org) and Grond.

Kite features simple and efficient handling of displacement data:

* Import InSAR displacement data from GAMMA, ISCE, GMTSAR and Matlab
* Efficient quadtree implementation
* Covariance estimation from noise
* Interactive GUI


## Installation and Requirement

```sh
sudo apt-get install python-pyside python-pyside.qtcore python-pyside.qtopengl python-yaml python-scipy python-numpy
git clone https://gitext.gfz-potsdam.de/isken/kite.git
cd kite
sudo pip install .
cd src/pyqtgraph
sudo pip install .
```

## Example
```python
from kite import Scene

# Import Matlab container to kite
scene = Scene.import_file('dataset.mat')
scene.spool()  # start the GUI for data inspection and Quadtree parametrisation

# Inspection of covariance parameters
scene.quadtree.covariance.plot()
```
