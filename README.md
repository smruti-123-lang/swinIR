# 🖼️ Image Super-Resolution using SwinIR

## 📌 Overview

This project implements **Single Image Super-Resolution (SISR)** using the **SwinIR (Swin Transformer for Image Restoration)** architecture in **PyTorch**. The model learns to reconstruct a high-resolution image from a low-resolution input image by leveraging transformer-based attention mechanisms.

The project uses the **DIV2K dataset** and performs **4× image upscaling** by generating low-resolution images through bicubic downsampling during training.

---

## 🚀 Features

* SwinIR-based Image Super-Resolution
* Custom PyTorch Dataset & DataLoader
* Bicubic downsampling for LR-HR pair generation
* 4× Image Upscaling
* End-to-End Training Pipeline
* GPU Training Support
* Model Checkpoint Saving
* Image Reconstruction using Transformer Architecture

---

## 🛠️ Tech Stack

* Python
* PyTorch
* Torchvision
* OpenCV
* PIL (Pillow)
* NumPy
* Matplotlib

---

## 📂 Dataset

The model is trained on the **DIV2K High Resolution Dataset**.

* 800 Training Images
* 100 Validation Images

High-resolution images are resized and converted into low-resolution images using bicubic interpolation to create LR-HR training pairs.

---

## 🏗️ Model Architecture

The project uses **SwinIR**, a Swin Transformer-based architecture designed for image restoration tasks.

Configuration:

* Upscale Factor: **4×**
* Input Size: **64 × 64**
* Output Size: **256 × 256**
* Window Size: **8**
* Embedding Dimension: **60**
* Upsampler: **PixelShuffle**

---

## ⚙️ Training

The training pipeline consists of:

1. Load HR image
2. Resize HR image
3. Generate LR image using bicubic interpolation
4. Convert images into tensors
5. Feed LR image into SwinIR
6. Compute L1 Loss with HR image
7. Update model using Adam Optimizer

Optimizer:

* Adam

Loss Function:

* L1 Loss

Learning Rate:

* 2e-4

---

## 📊 Results

The model successfully learns to reconstruct higher-resolution images from low-resolution inputs.

Example training loss:

```
Epoch 1  : 0.0465
Epoch 2  : 0.0432
Epoch 3  : 0.0432
Epoch 4  : 0.0425
Epoch 5  : 0.0427
Epoch 6  : 0.0429
Epoch 7  : 0.0420
Epoch 8  : 0.0424
Epoch 9  : 0.0412
Epoch 10 : 0.0409
```

The decreasing loss demonstrates that the model effectively learns image reconstruction.

---

## ▶️ How to Run

1. Clone the repository

```bash
git clone https://github.com/smruti-123-lang/swinIR.git
```

2. Install dependencies

```bash
pip install torch torchvision timm opencv-python pillow matplotlib numpy
```

3. Download the DIV2K dataset and update the dataset path.

4. Run the notebook to train the model.

---

## 📈 Future Improvements

* Train for 50–100 epochs for improved image quality
* Add PSNR and SSIM evaluation metrics
* Support real-world low-resolution images
* Fine-tune larger SwinIR variants
* Deploy as a web application using Streamlit or Flask

---

## 👩‍💻 Author

**Smruti Misra**

GitHub: https://github.com/smruti-123-lang
