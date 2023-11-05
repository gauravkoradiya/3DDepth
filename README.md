# 3DDepth
## Readthedocs

The document for 3D detection model design and Kitti and Waymo data training: https://mytutorial-lkk.readthedocs.io/en/latest/mydetector3d.html

The document for 3D detection based on V2X cooperative sensing data: https://mytutorial-lkk.readthedocs.io/en/latest/3DV2X.html



## Setup repo
Clone this repository, install this package (need NVIDIA CUDA environment)
```bash
sudo python setup.py develop
```

Install the SparseConv library from [spconv](https://github.com/traveller59/spconv) and [numba](https://numba.pydata.org/numba-doc/latest/user/installing.html):
```bash
pip install spconv-cu117 #pip install spconv-cu118
pip install numba
```

build additional cuda ops libraries via
```bash
(mycondapy39) [010796032@cs001 3DDepth]$ module load cuda-11.8.0-gcc-11.2.0-5tlywx3 #should match pytorch cuda version
(mycondapy39) [010796032@cs001 3DDepth]$ python mydetector3d/ops/setup.py build_ext --inplace
pip install nuscenes-devkit #required by nuscenes dataset
pip install efficientnet_pytorch==0.7.0 #required by lss
pip install pynvml
pip install nvidia-ml-py3 #required by import nvidia_smi
pip3 install --upgrade pyside2 pyqt5 #qt.qpa.plugin: Could not load the Qt platform plugin "xcb"
pip install kornia #required by BEVFusion
$ module load gcc/11.2.0
$ python cudasetup.py build_ext --inplace
```

Install 'mayavi' for 3d point cloud visualization.

## Kitti Dataset
Check [kittidata](Kitti/kittidata.md) for detailed information of Kitti dataset.

## Waymo Dataset
Check [waymodata](Waymo/waymodata.md) for detailed information of Waymo dataset.

