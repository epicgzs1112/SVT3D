#our new work for multi-view 3d reconstruction(voxel model)! paper is writing ,waiting for publish!
## Performance on shapnet dataset , IOU/F1 both ↑ .

|year|method|1view|2view|3view|4view| 5view|8view|12view|16view|20view|
|2016|3dr2n2(https://github.com/chrischoy/3D-R2N2)|1view|2view|3view|4view| 5view|8view|12view|16view|20view|
|2020|attsets(https://github.com/Yang7879/AttSets)|1view|2view|3view|4view| 5view|8view|12view|16view|20view|
|2020|pix2vox++(https://gitlab.com/hzxie/Pix2Vox)|1view|2view|3view|4view| 5view|8view|12view|16view|20view|
|2023|garnet(https://github.com/GaryZhu1996/GARNet)|1view|2view|3view|4view| 5view|8view|12view|16view|20view|
|----|----|----|----|----|----| ----|----|----|----|----|
|2021|evolt|1view|2view|3view|4view| 5view|8view|12view|16view|20view|
|2021|legoformer(https://github.com/faridyagubbayli/LegoFormer)|1view|2view|3view|4view| 5view|8view|12view|16view|20view|
|2021|3dretr(https://github.com/fomalhautb/3D-RETR)|1view|2view|3view|4view| 5view|8view|12view|16view|20view|
|year|umiformer(https://github.com/GaryZhu1996/UMIFormer)|1view|2view|3view|4view| 5view|8view|12view|16view|20view|
|year|lrgt(https://github.com/LiyingCV/Long-Range-Grouping-Transformer)|1view|2view|3view|4view| 5view|8view|12view|16view|20view|


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


