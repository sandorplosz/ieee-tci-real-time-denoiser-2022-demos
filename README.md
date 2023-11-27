# Introduction
This repository contains the executable for the paper S. Plosz, A. Maccarone, S. McLaughlin, G. S. Buller and A. Halimi, "Real-Time Reconstruction of 3D Videos from Single-Photon LiDaR Data in the Presence of Obscurants," in IEEE Transactions on Computational Imaging, doi: 10.1109/TCI.2023.3241547, [link](https://ieeexplore.ieee.org/document/10034858).

Citation:

    @ARTICLE{10034858,
    author={Plosz, Sandor and Maccarone, Aurora and McLaughlin, Stephen and Buller, Gerald S. and Halimi, Abderrahim},
    journal={IEEE Transactions on Computational Imaging}, 
    title={Real-Time Reconstruction of 3D Videos from Single-Photon LiDaR Data in the Presence of Obscurants}, 
    year={2023},
    pages={1-14},
    doi={10.1109/TCI.2023.3241547}}

The application performs depth and reflectivity estimation, denoising and 3D reconstruction of ToF data in real-time, and visualizes data in a 3D point cloud viewer.

The datasets for the demo can be downloaded from [this link](https://www.dropbox.com/scl/fo/qf3oejancf4itjqfhrwcw/h?rlkey=mqd3gc228nii31gayixc7zdhy&dl=0). This is real underwater LiDaR data acquired with a 192*128 SPAD array.

A video from the clear water experiment shows the reconstructed point-cloud along with images captured by RGB cameras:

https://user-images.githubusercontent.com/15447939/218517848-12057152-e37f-4689-8ce1-0b27259932d5.mp4

More videos from experiments in different AL (contaminated) water conditions can be found [here](https://www.dropbox.com/sh/lyi1piiuxa3qgpx/AABDsXaNwyrEk1R98kU6udCxa?dl=0).

# Requirements
- Windows computer (compiled with Visual Studio 2019 on Windows 10 x64)
- CUDA capable GPU (min. sm_50 Maxwell architecture)
- NVIDIA driver min. 452.39 (compiled with CUDA v11.6)

# Launching the demo
1. Downloaded the binary datasets and extract them to the data folder.
1. Edit config_quanticcam.cfg, set input_file for the data you want to process.
2. Launch hw.algo2.exe.
3. In the 3D viewer you can use the mouse to change the view.

# Configuration parameters
- You can launch the application paused by supplying the ***-paused*** command line option. You can step the processing of a frame by pressing a button on one of the 2D views. Pressing *space* will switch between paused and continous execution, and pressing *esc* will exit.
- You can disable the 2D or 3D views in the config file by setting parameters *enableVis2d* or *enableVis3d* to 0.
