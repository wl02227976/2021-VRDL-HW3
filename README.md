# 2021-VRDL-HW3

This repository is the official implementation of [2021 VRDL HW3](https://codalab.lisn.upsaclay.fr/competitions/333?secret_key=3b31d945-289d-4da6-939d-39435b506ee5). 


## Reproducing Submission
1. [Requirements](#Requirements)
2. [Pretrained_Model](#Pretrained_Model)
3. [Data](#Data)
4. [Inference](#Inference)

### Environment
-Anoconda



## Requirements

To install requirements:

```setup
#run the Anaconda Prompt
conda create -n hw3 python=3.7 -y
conda activate hw3

git clone https://github.com/wl02227976/2021-VRDL-HW3.git
cd 2021-VRDL-HW3

pip install -r requirements.txt
python setup.py install
```

## Pretrained_Model
Download the [model](https://drive.google.com/file/d/15GLAv1nd9LT2lZbQHNDoA4Yoi_rlu69Q/view?usp=sharing)

and put it in "2021-VRDL-HW3/model/"



## Data
Download the dataset from [here](https://drive.google.com/file/d/1WCOhLfEreUA-2H_J7NmgvN1hefuvEREs/view?usp=sharing)
and unzip it in "2021-VRDL-HW3/"


## Train

```Train
python nuclei_train.py --dir_log logs
```



## Inference

```Inference
python samples/nucleus/nucleus.py detect --dataset=dataset --subset=stage1_test --weights=model/mask_rcnn_nuclei_train_0026.h5
```
answer.json will be in "2021 VRDL HW3/"


## Reference
https://github.com/matterport/Mask_RCNN
https://github.com/wanwanbeen/maskrcnn_nuclei
https://stackoverflow.com/questions/49494337/encode-numpy-array-using-uncompressed-rle-for-coco-dataset
https://www.programcreek.com/python/example/120725/pycocotools.mask.encode
https://github.com/Jiankai-Sun/Modified-Mask-RCNN/blob/master/pycocotools/mask.py





