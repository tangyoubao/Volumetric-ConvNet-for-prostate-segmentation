## Volumetric-ConvNet-for-prostate-segmentation

This repository contains the network architecture and training script for network in "[Volumetric ConvNets with Mixed Residual Connections for Automated Prostate Segmentation from 3D MR Images](http://appsrv.cse.cuhk.edu.hk/~lqyu/papers/AAAI17_Prostate.pdf)".

## Caffe library

We slightly modify the original Caffe library to supporting the 3D operations. You can find the Caffe library in [https://github.com/yulequan/3D-Caffe](https://github.com/yulequan/3D-Caffe).

The main modification includes:
* ND support for CuDNN engine in "Convolution" layer 
* CuDNN engine for layer "Deconvolution"
* support for ND pooling in 'Pooling' layer
* Add randomly crop operation in "HDF5DataLayer"

For installation, please follow the offical instructions of [Caffe](http://caffe.berkeleyvision.org/installation.html).

The Caffe library has been tested successfully on Ubuntu 14.04 with CUDA 8.0 and CuDNN 5.0.

## Note
- We use **HDF5DataLayer** to read data. You need to  generate the hdf5 data from original data type.
