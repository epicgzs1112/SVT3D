#our new work for multi-view 3d reconstruction(voxel model)! paper is writing ,waiting for publish!
## Performance on shapnet dataset , IOU/F1 both ↑ .

|year|method|1view|2view|3view|4view| 5view|8view|12view|16view|20view|
| ---| -----| ----| --  | --- | -----|-----|-----|-----|-----|-----|
|2016ECCV|3dr2n2(https://github.com/chrischoy/3D-R2N2)|0.560/0.351|0.603/0.368|0.617/0.372|0.625/0.378| 0.634/0.382|0.635/0.382|0.636/0.382|0.636/0.382|0.636/0.383|
|2020IJCV|attsets(https://github.com/Yang7879/AttSets)|0.642/0.395|0.662/0.418|0.670/0.426|0.675/0.430| 0.677/0.432|0.685/0.444|0.688/0.445|0.692/0.447|0.693/0.448|
|2020IJCV|pix2vox++(https://gitlab.com/hzxie/Pix2Vox)|0.670/0.436|0.695/0.452|0.704/0.455|0.708/0.457| 0.711/0.458|0.715/0.459|0.717/0.460|0.718/0.461|0.719/0.462|
|2023PR|garnet(https://github.com/GaryZhu1996/GARNet)|0.673/0.418|0.705/0.455|0.716/0.468|0.722/0.475| 0.726/0.479|0.731/0.468|0.734/0.489|0.736/0.491|0.737/0.492|
|2021ICCV|evolt|/|/|/|0.609/0.358| /|0.698/0.448|0.720/0.475|0.729/0.486|0.735/0.492|
|2022ACCV|3D-C2FT(https://github.com/tiongleslie/3D-C2FT)|0.629/0.371|0.678/0.424|0.695/0.443|0.702/0.452| 0.708/0.458|0.716/0.468|0.720/0.476|0.723/0.477|0.725/0.479|
|2022CVPR|TMVNet|0.712/0.518|0.715/0.518|0.715/0.539|0.718/0.541| 0.718/0.546|0.719/0.546|0.719/0.547|0.721/0.550|/|
|2021arXiv.org|legoformer(https://github.com/faridyagubbayli/LegoFormer)|0.519|0.644|0.679|0.694| 0.703|0.713|0.717|0.719|0.721|
|2021BMVC|3dretr(https://github.com/fomalhautb/3D-RETR)|0.680|0.701|0.716|0.725| 0.736|0.739|0.747|0.755|0.757|
|2023ICCV|umiformer(https://github.com/GaryZhu1996/UMIFormer)|0.6802/0.4281|0.7384/0.4919|0.7518/0.5067|0.7573/0.5127| 0.7612/0.5168|0.7661/0.5213|0.7682/0.5232|0.7696/0.5245|0.7702/0.5251|
|2023ICCV|lrgt(https://github.com/LiyingCV/Long-Range-Grouping-Transformer)|0.6962/0.4461|0.7462/0.5005|0.7590/0.5148|0.7653/0.5214| 0.7692/0.5257|0.7744/0.5311|0.7766/0.5337|0.7781/0.5347|0.7786/0.5353|
|/|SVT3D([https://github.com/LiyingCV/Long-Range-Grouping-Transformer](https://github.com/epicgzs1112/SVT3D))|**0.7043/0.4575**|**0.7508/0.5070**|**0.736/0.5209**|**0.7686/0.5262**|** 0.7721/0.5296**|**0.7762/0.5338**|**0.7778/0.5358**|**0.7793/0.5374**|**0.7799/0.5383**|
##visual result on shapenet   waiting for .....
##Performance on shapnetchairrfc dataset , IOU/F1 both ↑ .waiting for ....
##visual result on shapenetchairrfc   waiting for .....
##visual result on pix3d waiting for ....

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


