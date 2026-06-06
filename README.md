# Brain Tumor Segmentation using MONAI 3D U-Net

## Overview

This project performs automatic brain tumor segmentation on MRI scans using a 3D U-Net architecture implemented with MONAI and PyTorch. The model was trained on the BraTS 2020 dataset and can identify tumor regions from multi-modal MRI images.

## Features

* Brain tumor segmentation from MRI scans
* 3D U-Net architecture using MONAI
* MRI preprocessing and normalization
* Multi-class tumor segmentation
* Ground Truth vs Prediction comparison
* Tumor overlay visualization
* Interactive Gradio interface

## Dataset

**BraTS 2020 (Brain Tumor Segmentation Challenge Dataset)**

MRI Modalities Used:

* T1
* T1CE
* T2
* FLAIR

Dataset preprocessing:

* Normalization
* Channel conversion
* Tensor transformation
* Multi-class mask generation

## Model Architecture

* Framework: PyTorch + MONAI
* Architecture: 3D U-Net
* Input Channels: 3
* Output Channels: 4
* Loss Function: DiceCELoss
* Optimizer: Adam
* Learning Rate: 1e-4

## Training Details

* Training Samples: 50
* Validation Samples: 20
* Epochs: 20
* GPU: Tesla T4

## Results

| Metric          | Value          |
| --------------- | -------------- |
| Validation Loss | ~0.39          |
| Architecture    | MONAI 3D U-Net |
| Dataset         | BraTS 2020     |

The model successfully learned tumor localization and generated segmentation masks that closely matched ground-truth annotations.

## Project Structure

Brain-Tumor-Segmentation/

├── app.py

├── train.py

├── brain_tumor_unet_final.pth

├── requirements.txt

├── README.md

├── results/

│   ├── result1.png

│   ├── result2.png

│   ├── result3.png

│   ├── result4.png

│   └── result5.png

## Installation

```bash
pip install torch
pip install monai
pip install numpy
pip install matplotlib
pip install gradio
```

## Run Training

```bash
python train.py
```

## Run Application

```bash
python app.py
```

## Technologies Used

* Python
* PyTorch
* MONAI
* NumPy
* Matplotlib
* Gradio
* Medical Imaging
* Deep Learning

## Future Improvements

* Train on full BraTS dataset
* Deploy on Hugging Face Spaces
* Improve segmentation accuracy
* Add support for NIfTI (.nii) files
* Add 3D tumor visualization

## Author

Nandan

AI & Machine Learning Engineering Student

## License

This project is intended for educational and research purposes only.
