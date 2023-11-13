# MoCha-Stereo

https://github.com/anonymousrecognition/anonymous/assets/135130121/f4e8eae1-7fa8-452d-8593-683e37d32d34

As of this work submission, MoCha-Stereo ranks #1 at [KITTI-2015](https://www.cvlibs.net/datasets/kitti/eval_scene_flow.php?benchmark=stereo) and #1 at [KITTI-2012](https://www.cvlibs.net/datasets/kitti/eval_stereo_flow.php?benchmark=stereo&table=refl&error=3&eval=all) Reflective. Our code will be available after been accepted.

## TODO List
- [ ] Demos
- [ ] Code of MoCha-Stereo
- [ ] Code of MoCha-MVS
      
## Environment
* NVIDIA Tesla A6000
* Python 3.8.16
* Pytorch 1.12.0
* CUDA 11.3

## Requirements

## Data Preparation
To evaluate/train MoCha, you will need to download the required datasets. 
* [Sceneflow](https://lmb.informatik.uni-freiburg.de/resources/datasets/SceneFlowDatasets.en.html#:~:text=on%20Academic%20Torrents-,FlyingThings3D,-Driving) (Includes FlyingThings3D, Driving & Monkaa)
* [Middlebury](https://vision.middlebury.edu/stereo/data/)
* [KITTI](http://www.cvlibs.net/datasets/kitti/eval_scene_flow.php?benchmark=stereo)
* [ETH3D](https://www.eth3d.net/datasets#low-res-two-view-test-data)

By default `stereo_datasets.py` will search for the datasets in these locations. 

```
├── /datasets
    ├── sceneflow
        ├── frames_finalpass
        ├── disparity
    ├── KITTI
        ├── KITTI_2012
            ├── training
            ├── testing
        ├── KITTI_2015
            ├── training
            ├── testing
    ├── Middlebury
        ├── MiddEval3
            ├── trainingF
            ├── testF
    ├── ETH3D
        ├── two_view_testing
```


