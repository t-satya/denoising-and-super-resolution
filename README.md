# 🌒 Low-Light Image Enhancement

This project focuses on improving noisy, low-resolution images captured in dark conditions. It uses a custom two-stage deep learning model in PyTorch that performs **denoising** followed by **4× super-resolution**.

---

## 🧠 Model Overview

- `CombinedModel` = `LightweightDenoiser` + `SuperResolutionNetLAKD`
- Built using PyTorch
- Output: Enhanced images with reduced noise and 4× resolution

---

## ⚙️ Training Setup

- Loss: `MSELoss` (optimizes PSNR indirectly)
- Optimizer: Adam (`lr=1e-4`)
- Epochs: 200
- Device: GPU (`cuda`) with `nn.DataParallel` and mixed precision (`torch.amp`)
- Best model saved as `best_model.pth`

---

## 🧪 Evaluation

- Metric: **PSNR (Peak Signal-to-Noise Ratio)**
- Validated on unseen low-light images

---

## 📁 Files

- `denoising and super resolution of low light images.ipynb`: Full notebook

---

## 🚀 Planned Improvements

- Add perceptual or SSIM loss for more visually realistic outputs
- Explore GAN-based models like SRGAN
- Build a Streamlit/Gradio app for real-time enhancement
- Train on larger datasets (LOL, SIDD)


