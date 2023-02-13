# Introduction
This repository contains the executable for the paper "Real-Time Reconstruction of 3D Videos from Single-Photon LiDaR Data in the Presence of Obscurants" published in IEEE TCI, [link](https://ieeexplore.ieee.org/document/10034858)

Citation:

    @ARTICLE{10034858,
    author={Plosz, Sandor and Maccarone, Aurora and McLaughlin, Stephen and Buller, Gerald S. and Halimi, Abderrahim},
    journal={IEEE Transactions on Computational Imaging}, 
    title={Real-Time Reconstruction of 3D Videos from Single-Photon LiDaR Data in the Presence of Obscurants}, 
    year={2023},
    pages={1-14},
    doi={10.1109/TCI.2023.3241547}}

The application performs depth and reflectivity estimation, denoising and 3D reconstruction of ToF data real-time, and visualizes data in a 3D point cloud viewer.

**The datasets for the demos will be made available shortly!** These are real underwater LiDaR data acquired with a 192*128 SPAD array.

A video from the clear water experiment shows the processed point-cloud along with images captured by RGB cameras:

https://user-images.githubusercontent.com/15447939/218517848-12057152-e37f-4689-8ce1-0b27259932d5.mp4

More videos from experiments in different AL (contaminated) water conditions can be found [here](https://www.dropbox.com/home/fast_denoiser_videos).

# Requirements
- Windows computer (compiled on win 10)
- CUDA capable GPU

# Launching the demo
1. Downloaded the binary datasets and extract them to the data folder.
1. Edit config_qunaticcam.cfg, set input_file for the data you want to process.
2. Launch hw.algo2.exe.
3. In the 3D viewer you can use the mouse to change the view.

# Configuration parameters
- You can launch the application paused by supplying the ***-paused*** command line option. You can step the processing of a frame by pressing a button on one of the 2D views. Pressing *space* will switch between paused and continous execution, and pressing *esc* will exit.
- You can disable the 2D or 3D views in the config file by setting parameters *enableVis2d* or *enableVis3d* to 0.
