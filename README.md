# Satellite Image Super-Resolution with GAN

## Project Overview
This project aims to enhance the resolution of satellite images using deep learning techniques, particularly ESRGAN (Enhanced Super-Resolution Generative Adversarial Networks). The goal is to upscale images from 416 × 416 to higher resolutions (e.g., 832 × 832) while preserving details.

## Why This Project?
Satellite images are often available at lower resolutions due to sensor limitations or storage constraints. High-resolution images are crucial for:
- **Urban planning** 
- **Disaster management** 
- **Environmental monitoring** 
- **Agricultural analysis** 

Super-resolution helps improve the quality of satellite imagery for these applications.

##  Approach
We use **GAN**, which consists of:
1. **Generator:** A deep CNN that learns to upscale low-resolution images.
2. **Discriminator:** Distinguishes real high-resolution images from generated ones.
3. **Perceptual Loss:** Uses pre-trained VGG to preserve high-level image details.

## Implementation Steps
1. **Dataset Preparation**
   - Collect satellite images
   - Organize them into Low-Resolution (LR) and High-Resolution (HR) folders

2. **Data Preprocessing**
   - Resize images to required dimensions
   - Normalize and convert them into tensors

3. **Model Training**
   - Train ESRGAN on paired LR-HR images
   - Use adversarial loss, content loss, and pixel-wise loss

4. **Inference & Evaluation**
   - Apply the trained model to enhance satellite images
   - Evaluate performance using PSNR, SSIM

## Folder Structure
```
│── data/
│   ├── LR/  # Low-resolution images
│   ├── HR/  # High-resolution images
│── notebooks/  # Jupyter Notebooks
│── README.md
```

## Installation & Setup
```sh
git clone https://github.com/1103Dkpatel/project11__jjaayygguurruuddeevv.git
cd Satellite-SuperResolution
pip install -r requirements.txt
```
