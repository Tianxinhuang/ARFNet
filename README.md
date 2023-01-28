# ARFNet
The codes for Adaptive Recurrent Forward Network for Dense Point Cloud Completion published by TMM. This work is the enhanced version of [RFNet](https://github.com/Tianxinhuang/RFNet) published in ICCV2021. It works by replacing the parameter-controlled merge layer in RFNet with network-controlled Adamerge module. Refine Cell in RFNet is not used in this work for efficiency, which can also be added to further improve the performances.

## Environment
* TensorFlow 1.13.1
* Cuda 10.0
* Python 3.6.9
* lmdb 0.98  
* tensorpack 0.10.1
* numpy 1.14.5

## Dataset
The adopted dataset can be found in [PCN](https://github.com/wentaoyuan/pcn).

## Usage

1. Compile

```
cd ./tf_ops
bash compile.sh
```

2. Train

```
Python3 vv_recon.py
```
Note that the paths of training data(`trainpath`) and validation data(`valpath`) should be edited according to your setting.

3. Test

```
Python3 recon_test.py
```
The paths of test data(`data_dir`) and lists(`list_path`) should be edited before testing.
The qualitative results should be 

![image](https://github.com/Tianxinhuang/ARFNet/blob/master/tmm_quali.jpg)

The quantitative results on the Known categories of ShapeNet in PCN would be
![image](https://github.com/Tianxinhuang/ARFNet/blob/master/tmm_quan.jpg)

## Citation
If you find our work useful for your research, please cite:
```
@article{huang2022adaptive,
  title={Adaptive Recurrent Forward Network for Dense Point Cloud Completion},
  author={Huang, Tianxin and Zou, Hao and Cui, Jinhao and Zhang, Jiangning and Yang, Xuemeng and Li, Lin and Liu, Yong},
  journal={IEEE Transactions on Multimedia},
  year={2022},
  publisher={IEEE}
}
```
