#our new work for multi-view 3d reconstruction(voxel model)! paper is writing ,waiting for publish!
## Installation
The environment was tested on Ubuntu 22.04LTS and. We trained SVT3D on 1 3060 with 12 GB  for about 3 days.CUDA 11.3 torch 1.11.0 .
just pip install   xxxx.    no module named xxxx.  
or just create env from environment.yml file
conda env create -f environment.yml
conda activate SVT3D

## Datasets

We use the [ShapeNet](https://www.shapenet.org/),ShapeNetChairRFC and [Pix3D](http://pix3d.csail.mit.edu/) in our experiments, which are available below:

- ShapeNet rendering images: http://cvgl.stanford.edu/data2/ShapeNetRendering.tgz
- ShapeNet voxelized models: http://cvgl.stanford.edu/data2/ShapeNetVox32.tgz
- ShapeNetChairRFC:https://drive.google.com/file/d/1gehwNVpSfd_olXYVspF6wHKf6_UPLa7m/view?usp=drive_link
- Pix3D images & voxelized models: http://pix3d.csail.mit.edu/data/pix3d.zip


## Get start
pretrained weight on 3 view:https://drive.google.com/drive/folders/1v7WxCu5LNpg7K6Q_1fq2LAj5isgB-AKK?usp=drive_link
### Training
after ensure the dataset path is right in config.py,just run the runner.py.
-config.py   -> runner.py


### Evaluation
when eval just add --test --weights pathtoweight   paprameter in  correspond runner.py   file . 
-config.py   -> runner.py  --test --weights pathtoweight trained on shapnet    eval on shapenet


