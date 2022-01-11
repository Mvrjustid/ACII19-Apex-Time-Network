# ACII19-Apex-Time-Network
[![GitHub stars](https://img.shields.io/github/stars/Mvrjustid/ACII19-Apex-Time-Network)](https://github.com/Mvrjustid/ACII19-Apex-Time-Network)
[![GitHub folks](https://img.shields.io/github/forks/Mvrjustid/ACII19-Apex-Time-Network)](https://github.com/Mvrjustid/ACII19-Apex-Time-Network)
[![GitHub issues](https://img.shields.io/github/issues/Mvrjustid/ACII19-Apex-Time-Network)](https://github.com/Mvrjustid/ACII19-Apex-Time-Network/issues)
[![My achievement](https://img.shields.io/badge/Milestone-1st%20ACII-orange)](https://scholar.google.com/citations?user=H7VBxLgAAAAJ&hl=en)

A Novel Apex-Time Network for Cross-Dataset Micro-Expression Recognition
  
  
  
# Platforms and dependencies
Ubuntu 16.04  Python 2.7  CUDA8.0 CuDNN6.0+  
Caffe：https://github.com/BVLC/caffe/
  
  
  
# Prepare
* Download the database (optional)  
  CASMEII: http://fu.psych.ac.cn/CASME/casme2-en.php  
  SAMM: http://www2.docm.mmu.ac.uk/STAFF/m.yap/dataset.php  
  SMIC: https://www.oulu.fi/cmvs/node/41319  
  
* if you want to download the original database, the **Data** fold contain all the needed data for this repositories.  
  1. **Add_python_layers** contains a *.py* scrip that is for image and point data loading in Caffe.  
  2. **Apex_Cropped_images** contains all the Apex frames of three Database (namely: CASMEII   SAMM   SMIC).                  **Apex_Cropped_images.txt** contains image root and label in **Apex_Cropped_images** fold.  
  3. **OpticalFlowFeatureData.txt** is the temporal features described in our paper.  
    
  
  
# ATNet
This fold is our proposed network for Cross-Dataset Micro-Expression Recognition.  
  
* **CDE** is the Composite Database Evaluation. For CASMEII_sub01, it means all samples (from the full consolidated database) are used for training except sub01 in CASMEII.  
  
* **HDE** is the Holdout-Database Evaluation. For TEST_CASMEII, it means the model is trained on two datasets(SAMM SMIC) and tested on CASMEII.  

* Notice: for each tries, you can use the *get_samples_Train_Test_TXT.py* to get the .txt list.
  
* How to run  
Take the CASMEII_sub01 fold for example, you just need to change your root to ../ACII19-Apex-Time-Network-master/, and then run: 
sh train_net.sh 
in the terminal.  
  
  
# MicroAttentionNet(Compared)
This fold is the compared method used in our paper.  
  
Micro-Attention outperformed the method described in the paper "From Macro to Micro Expression Recognition: Deep Learning on Small Datasets Using Transfer Learning", the latter one won the first place in the Facial Micro-Expression Grand Challenge (MEGC2018) at FG 2018.
  
  
  
# LBP-TOP(Compared)
This fold is the compared method used in our paper.  
  
Features.zip contained all the LBP-TOP features.   
  
  
# HOOF(Compared)
This fold is the compared method used in our paper.  
  
Features.zip contained all the HOOF features.  
The optical method for HOOF is refer to https://www.researchgate.net/publication/320373402_Dual_Temporal_Scale_Convolutional_Neural_Network_for_Micro-Expression_Recognition
  
  
  
# Citation
  
If it is helpful, please cite:  
```
@inproceedings{peng2019novel,
  title={A novel apex-time network for cross-dataset micro-expression recognition},
  author={Peng, Min and Wang, Chongyang and Bi, Tao and Shi, Yu and Zhou, Xiangdong and Chen, Tong},
  booktitle={2019 8th International Conference on Affective Computing and Intelligent Interaction (ACII)},
  pages={1--6},
  year={2019},
  organization={IEEE}
}
```
```
@article{wang2020micro,
  title={Micro-attention for micro-expression recognition},
  author={Wang, Chongyang and Peng, Min and Bi, Tao and Chen, Tong},
  journal={Neurocomputing},
  volume={410},
  pages={354--362},
  year={2020},
  publisher={Elsevier}
}
```

