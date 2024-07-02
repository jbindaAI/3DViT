# Moving toward 3D Vision Transformers
<div align="center">
  <img src="deepvision.png" alt="Logo" width="200"/>
</div>


## Overview
This repository contains code needed to reproduce results of `Moving toward 3D Vision Transformers` project. This project aimed to develop 3D ViT models leveraging pre-trained weights from foundational vision DINO model, according to weight inflation procedure. 3DViTs were fine-tuned without inflation, with average inflation and with centering inflation of embedding weights. Achieved models were compared with baseline 2D models.


### Prerequisites:
1. Clone repository and move into project directory:
```bash
git clone https://github.com/jbindaAI/3DViT.git
cd 3DViT
```
2. Create python virtual environment:
```python
python3 -m venv venv
```
3. Activate virtual environment and install requirements:
```bash
source venv/bin/activate
pip3 install -r requirements.txt
```
4. Download LIDC-IDRI dataset and preprocess it: </br>
Dataset is available there: [LIDC-IDRI](https://www.cancerimagingarchive.net/collection/lidc-idri/). To download it, follow publisher instructions. </br>
Data preprocessing should be done as in a paper: [Integration of Radiomics and Tumor Biomarkers in Interpretable Machine Learning Models](https://doi.org/10.3390/cancers15092459). </br>
I have preprocessed data in batches with `dataset_creation.py` script.

5. Create empty directory and download into it pretrained DINO backbone: </br>
It is required to instantiate 3DViT.
```bash
mkdir pretrained
cd pretrained
wget https://dl.fbaipublicfiles.com/dino/dino_vitbase16_pretrain/dino_vitbase16_pretrain.pth
cd ..
```

7. Download already preprocessed data: [OPTIONAL] </br>
If you want to faster make your setup, you can directly download `dataset.tar.gz` file containing preprocessed dataset. </br>
Download: [Google Disc](https://drive.google.com/file/d/1zWsmqwdAMKKcz3hvbc4CFXh6MRIM7Yw9/view?usp=sharing)
It contains everything you need to perform training/evaluation -> nodule crops, fitted normalization factors, dataset splitting pattern. </br>
You may find useful command for downloading things from google disc:
```bash
gdown https://drive.google.com/uc\?id\=1zWsmqwdAMKKcz3hvbc4CFXh6MRIM7Yw9    
```
   
9. Download already fine-tuned checkpoints: [OPTIONAL] </br>
All checkpoints (~102GB): Available on a request. </br>
Only versions v0: [Google Disc]() </br>
```bash
gdown https://drive.google.com/uc\?id\=1zWsmqwdAMKKcz3hvbc4CFXh6MRIM7Yw9    
```

## Author
Jakub Binda

## Licence
MIT

Logo is AI generated
[https://logo.com/](https://logo.com/)