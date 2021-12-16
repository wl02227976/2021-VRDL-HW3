# 2021-VRDL-HW2

This repository is the official implementation of [2021 VRDL HW2](https://competitions.codalab.org/competitions/35888?secret_key=7e3231e6-358b-4f06-a528-0e3c8f9e328e#participate-submit_results). 


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
conda create -n hw2 python=3.7 -y
conda activate hw2
conda install pytorch torchvision torchaudio cudatoolkit=10.2 -c pytorch

git clone https://github.com/wl02227976/2021-VRDL-HW2
cd 2021-VRDL-HW2

pip install -r requirements.txt
```

## Pretrained_Model
Download the [runs.zip](https://drive.google.com/drive/folders/1rcPvAKc6IzfcppW4ShS8HRmYsaB6llvk?usp=sharing)

and unzip it in "2021-VRDL-HW2/"



## Data
Download the dataset(test.zip and train.zip) from [here](https://drive.google.com/drive/folders/1rcPvAKc6IzfcppW4ShS8HRmYsaB6llvk?usp=sharing)
and put them into the "data" folder and unzip them

```data
python data_preprocess.py
```

create the folder named "valid" in "data" folder
put 30001.png-33402.png(in "/data/train/") and 30001.txt-33402.txt(in "/data/train/") into "valid"folder

## Train
Download the [yolov5m.pt](https://github.com/ultralytics/yolov5/releases)
and put it in "2021-VRDL-HW2/weights"
```Train
python train.py --img 320 --batch 16 --epochs 50 --data svhn.yaml --weights yolov5m.pt
```



## Inference
Use [colab](https://drive.google.com/file/d/1k6zzedxfWwQWVEILrc5_faeMqtlFDfiP/view?usp=sharing)
or

```Inference
python detect.py --source data/test/ --weights runs/train/exp3/weights/hw2.pt --conf 0.25 --save-txt --save-conf
python answer.py
```
answer.json will be in "2021 VRDL HW2/"


## Reference
https://github.com/ultralytics/yolov5/releases
https://blog.csdn.net/iteapoy/article/details/117899064
https://www.vitaarca.net/post/tech/access_svhn_data_in_python/





