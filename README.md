# DepthFlow

This is the official PyTorch implementation of our paper:

> **DepthFlow: Exploiting Depth-Flow Structural Correlations for Unsupervised Video Object Segmentation**, *ICCVW 2025*\
> Suhwan Cho, Minhyeok Lee, Jungho Lee, Donghyeong Kim, Sangyoun Lee\
> Link: [[arXiv]](https://arxiv.org/abs/2507.19790)


<img src="https://github.com/user-attachments/assets/dcbd818a-fff9-417f-a2cf-631df4c82df8" width=800>


You can also find other related papers at [awesome-video-object-segmentation](https://github.com/suhwan-cho/awesome-video-object-segmentation).


## Abstract
In unsupervised VOS, the scarcity of training data has been a significant bottleneck in achieving high segmentation accuracy. Inspired by 
observations on two-stream approaches, we introduce a novel data generation method based on the **depth-to-flow conversion** process. With our flow synthesis protocol,
large-scale image-flow-mask triplets can be leveraged during network training. To facilitate future research, we also prepare the **DUTSv2** dataset that includes 
pairs of original images and their corresponding synthetic flow maps.

## Setup
1\. Download the datasets:
[DUTS](http://saliencydetection.net/duts/#org3aad434), 
[DAVIS](https://davischallenge.org/davis2017/code.html),
[FBMS](https://lmb.informatik.uni-freiburg.de/resources/datasets),
[YouTube-Objects](https://data.vision.ee.ethz.ch/cvl/youtube-objects),
[Long-Videos](https://www.kaggle.com/datasets/gvclsu/long-videos).

2\. Estimate and save optical flow maps from the videos using [RAFT](https://github.com/princeton-vl/RAFT).

3\. For DUTS, simulate optical flow maps using [DPT](https://github.com/isl-org/DPT).

4\. I also provide the pre-processed datasets:
[DUTSv2](https://drive.google.com/file/d/1P8_USG8CWlpWm5UEcfXgXdr3IYQnhAvi/view?usp=drive_link), 
[DAVIS](https://drive.google.com/file/d/1kx-Cs5qQU99dszJQJOGKNb-wD_090q6c/view?usp=drive_link), 
[FBMS](https://drive.google.com/file/d/1Zgt5ouwFeTpMTemfNeEFz7uEUo77e2ml/view?usp=drive_link), 
[YouTube-Objects](https://drive.google.com/file/d/1t_eeHXJ30TWBNmMzE7vfS0izEafiBfgn/view?usp=drive_link),
[Long-Videos](https://drive.google.com/file/d/1gZm1QBT_6JmHhphNrxuSztcqkm_eI6Sq/view?usp=drive_link).


##  Running 

### Training
Start DepthFlow training with:
```
python run.py --train
```

Verify the following before running:\
✅ Training dataset selection and configuration\
✅ GPU availability and configuration\
✅ Backbone network selection


### Testing
Run DepthFlow with:
```
python run.py --test
```

Verify the following before running:\
✅ Testing dataset selection\
✅ GPU availability and configuration\
✅ Backbone network selection\
✅ Pre-trained model path


## Attachments
[Pre-trained model (mitb0)](https://drive.google.com/file/d/1nu3qcU2Ot8Ly-5RPGBkYBMIW3Y6l6_wm/view?usp=drive_link)\
[Pre-trained model (mitb1)](https://drive.google.com/file/d/1rJGP4a_AwD4OHzx7CaVt2_fctGtwWoA5/view?usp=drive_link)\
[Pre-trained model (mitb2)](https://drive.google.com/file/d/1StngTtpxtR10-RP2OxtYpZTs3SdePJua/view?usp=drive_link)\
[Pre-computed results](https://drive.google.com/file/d/1Umb5rGtVir8PwHsuFumYIkv49ALcE1Cl/view?usp=drive_link)

## Contact
Code and models are only available for non-commercial research purposes.\
For questions or inquiries, feel free to contact:
```
E-mail: suhwanx@gmail.com
```
