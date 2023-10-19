# MoCha for stereo matching
As of this work submission, MoCha ranks #1 at [KITTI-2015](https://www.cvlibs.net/datasets/kitti/eval_scene_flow.php?benchmark=stereo) and #1 at [KITTI-2012](https://www.cvlibs.net/datasets/kitti/eval_stereo_flow.php?benchmark=stereo&table=refl&error=3&eval=all) Reflective. Our code will be available after been accepted.

## TODO List
- [ ] Demos
- [ ] Code of MoCha
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
```

## (Optional) Faster Implementation

A faster CUDA implementation of the correlation sampler is provided, which works with mixed precision feature maps.
```Shell
cd sampler && python setup.py install && cd ..
```
Running `demo.py`, `train_stereo.py` or `evaluate.py` with `--corr_implementation reg_cuda` together with `--mixed_precision` will speed up the model without impacting performance.

To significantly decrease memory consumption on high resolution images, use `--corr_implementation alt`. While this implementation is slower than the default.

