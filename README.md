# Multi-Drone-Multi-Object-Detection-and-Tracking


## Installation
1.create a conda virtual environment and activate it:
    
    conda create -n mdmt python=3.8
    conda activate mdmt

2.install pytorch and suited mmcv-full, please refer to ![MMtracking](https://github.com/open-mmlab/mmtracking/blob/master/docs/en/install.md).

(if you have no idea which version to install, stay with ours:
torch                          1.10.0+cu113/
torchvision                    0.11.1+cu113/
mmcv-full                      1.5.0/
mmdet                          2.25.1)

3.download the codes and :
    
    cd Multi-Drone-Multi-Object-Detection-and-Tracking-main
    pip install -r requirements.txt
    cd mmdet
    pip install -r requirements/build.txt
    pip install -v -e .  # or "python setup.py develop"
    cd ..
    pip install -r requirements.txt
    pip install -v -e .  # or "python setup.py develop"


## Getting started
### Dataset Structure
> Multi-Drone-Multi-Object-Detection-and-Tracking-main
>> data
>>> MDMT
>>>> train/
>>>> val/
>>>> test/
### Inference
Inference MIA-Net:

    python ./demo/supplement_MIA.py
Inference MIA-Net(w/o supplementation), MIA-Net(w/ localmatching), MIA-Net(w/ globalmatching), run:
    
    python ./demo/multiDrone_matchingIDallocation-NMS.py
    python ./demo/multiDrone_localmatching-NMS.py
    python ./demo/multiDrone_globalmatching-NMS.py
### Evaluation
For tracking perforcement:

    python ./demo/eval/json_2_txt.py
    python ./demo/eval/txttxt_test.py

For MDA score:

    python ./demo/eval/mango_eval.py


<!-- ## FAQ
Please refer to ![FAQ](https://github.com/Edision-liu/Multi-Drone-Multi-Object-Detection-and-Tracking/edit/main/README.md) for frequently asked questions. -->


## Citation

