# *MVP Benchmark:* Multi-View Partial Point Clouds for Completion and Registration

[[Website]](https://mvp-dataset.github.io/)

<p align="center"> 
<img src="images/logo.png">
</p>


## [NEWS]
- **2021-12-22 [NEW:tada:]** The workshop report is avaliable at [Arxiv](https://arxiv.org/pdf/2112.12053.pdf)!
- **2021-10-17 [NEW:tada:]** Awards at ICCV2021 Workshop. Congradulations to all the winner teams!
- **2021-07-12** The submission on [Codalab](https://competitions.codalab.org/competitions/33430) starts!
- **2021-07-10** [Database website](https://mvp-dataset.github.io) and [Challenge website](https://competitions.codalab.org/competitions/33430) are online!
- **2021-07-09** Code and data released!
- **2021** The MVP challenges will be hosted in the **ICCV2021 Workshop**: ***[Sensing, Understanding and Synthesizing Humans](https://sense-human.github.io/)***.

## [Timeline]
- ~~**2021-07-12**&nbsp;&nbsp;  Submission start date~~
- ~~**2021-09-12**&nbsp;&nbsp;  Public submission deadline~~
- ~~**2021-09-19**&nbsp;&nbsp;  Private submission deadline~~
- ~~**2021-10-04**&nbsp;&nbsp;  Technical report deadline~~
- ~~**2021-10-17**&nbsp;&nbsp;  Awards at ICCV2021 Workshop~~


## [MVP Benchmark]

### Overview
This repository introduces the MVP Benchmark for partial point cloud **[COMPLETION](https://github.com/paul007pl/MVP_Benchmark/tree/main/completion)** and **[REGISTRATION](https://github.com/paul007pl/MVP_Benchmark/tree/main/registration)**, and it also includes following recent methods:

+ **Completetion:**
    &nbsp;&nbsp;[1] [PCN](https://github.com/wentaoyuan/pcn); &nbsp;&nbsp;[2] [ECG](https://github.com/paul007pl/ECG); &nbsp;&nbsp;[3] [VRCNet](https://github.com/paul007pl/VRCNet)

+ **Registration:**
    &nbsp;&nbsp;[1] [DCP](https://github.com/WangYueFt/dcp); &nbsp;&nbsp;[2] [DeepGMR](https://github.com/wentaoyuan/deepgmr); &nbsp;&nbsp;[3] [IDAM](https://github.com/jiahaowork/idam)

This repository is implemented in Python 3.7, PyTorch 1.5.0, CUDA 10.1 and gcc > 5. 


### Installation
Install [Anaconda](https://docs.anaconda.com/anaconda/install/index.html), and then use the following command:
```
git clone --depth=1 https://github.com/paul007pl/MVP_Benchmark.git
cd MVP_Benchmark; source setup.sh;
```
If your connection to conda and pip is unstable, it is recommended to manually follow the setup steps in `setup.sh`.


### MVP Dataset
Download corresponding dataset:
  + **Completion** :&nbsp;&nbsp;&nbsp;&nbsp; [Google Drive](https://drive.google.com/drive/folders/1XxZ4M_dOB3_OG1J6PnpNvrGTie5X9Vk_) &nbsp;&nbsp; or &nbsp;&nbsp; [百度网盘](https://pan.baidu.com/s/18pli79KSGGsWQ8FPiSW9qg)&nbsp;&nbsp;(code: p364)
  + **Registration** :&nbsp;&nbsp;&nbsp;&nbsp; [Google Drive](https://drive.google.com/drive/folders/1RlUW0vmmyqxkBTM_ITVguAjxzIS1MFz4) &nbsp;&nbsp; or &nbsp;&nbsp; [百度网盘](https://pan.baidu.com/s/18pli79KSGGsWQ8FPiSW9qg)&nbsp;&nbsp;(code: p364)


### Usage
For both completion and registration:
  + `cd completion` or `cd registration`
  + To train a model: run `python train.py -c ./cfgs/*.yaml`, e.g. `python train.py -c ./cfgs/pcn.yaml`
  + To test a model: run `python test.py -c ./cfgs/*.yaml`, e.g. `python test.py -c ./cfgs/pcn.yaml`
  + Config for each algorithm can be found in `cfgs/`.
  + `run_train.sh` and `run_test.sh` are provided for SLURM users. 


+ Different partial point clouds for the same CAD Model:
<p align="center"> 
<img src="images/partial_pcds.gif", style="zoom: 75%;">
</p>

+ High-quality complete point clouds:
<p align="center"> 
<img src="images/complete_pcds.gif", style="zoom: 75%;">
</p>

<br>


## [Citation]
If you find our code useful, please cite our paper:
```bibtex
@inproceedings{pan2021variational,
  title={Variational Relational Point Completion Network},
  author={Pan, Liang and Chen, Xinyi and Cai, Zhongang and Zhang, Junzhe and Zhao, Haiyu and Yi, Shuai and Liu, Ziwei},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  pages={8524--8533},
  year={2021}
}
@article{pan2021robust,
  title={Robust Partial-to-Partial Point Cloud Registration in a Full Range},
  author={Pan, Liang and Cai, Zhongang and Liu, Ziwei},
  journal={arXiv preprint arXiv:2111.15606},
  year={2021}
}
@article{pan2021mvp, 
  title={Multi-View Partial (MVP) Point Cloud Challenge 2021 on Completion and Registration: Methods and Results}, 
  author={Pan, Liang and Wu, Tong and Cai, Zhongang and Liu, Ziwei and Yu, Xumin and Rao, Yongming and Lu, Jiwen and Zhou, Jie and Xu, Mingye and Luo, Xiaoyuan and Fu, Kexue, and Gao, Peng, and Wang, Manning, and Wang, Yali, and Qiao, Yu, and Zhou, Junsheng, and Wen, Xin, and Xiang, Peng, and Liu, Yu-Shen, and Han, Zhizhong, and Yan, Yuanjie, and An, Junyi, and Zhu, Lifa, and Lin, Changwei, and Liu, Dongrui, and Li, Xin, and G ́omez-Fern ́andez, Francisco, and Wang, Qinlong, and Yang, Yang}, 
  journal={arXiv preprint arXiv:2112.12053},
  year={2021}
}
```

<br>


## [License]
Our code is released under Apache-2.0 License.

<br>


## [Acknowledgement]
We include the following PyTorch 3rd-party libraries:  
[1] [CD](https://github.com/ThibaultGROUEIX/ChamferDistancePytorch)  
[2] [EMD](https://github.com/Colin97/MSN-Point-Cloud-Completion)  
[3] [MMDetection3D](https://github.com/open-mmlab/mmdetection3d)  

We include the following algorithms:  
[1] [PCN](https://github.com/wentaoyuan/pcn)  
[2] [ECG](https://github.com/paul007pl/ECG)  
[3] [VRCNet](https://github.com/paul007pl/VRCNet)  
[4] [DCP](https://github.com/WangYueFt/dcp)  
[5] [DeepGMR](https://github.com/wentaoyuan/deepgmr)  
[6] [IDAM](https://github.com/jiahaowork/idam)  
