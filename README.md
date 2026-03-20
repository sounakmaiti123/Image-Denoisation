# 🧠 Intelligent Image Denoising using DSP + Autoencoder

<p align="center">
  <img src="https://media.giphy.com/media/3o7TKtnuHOHHUjR38Y/giphy.gif" width="300"/>
</p>

---

## 🚀 Project Overview

This project presents a **hybrid Digital Signal Processing (DSP) + Deep Learning approach** for denoising MRI images.

Noise in medical images degrades quality and affects diagnosis.
This system combines:

* 🧮 Classical DSP Filters (Gaussian & Median)
* 🤖 Deep Learning Model (Convolutional Autoencoder)

to reconstruct high-quality images from noisy inputs.

---

## 🧠 System Architecture

```
MRI Dataset
     ↓
Preprocessing
     ↓
Noise Addition
     ↓
DSP Filtering (Gaussian / Median)
     ↓
Autoencoder (Encoder → Bottleneck → Decoder)
     ↓
Denoised Output
```

---

## ⚙️ Technical Workflow

* Load MRI dataset (~14,000 images)
* Resize to 128×128 grayscale
* Normalize pixel values (0–1)
* Add Gaussian noise
* Apply DSP filters:

  * Gaussian Blur
  * Median Filter
* Train Autoencoder:

  * Input: Noisy Image
  * Output: Clean Image
* Reconstruct denoised images

---

## 🏗️ Autoencoder Architecture

```
Input (128x128x1)
   ↓
Conv2D + ReLU
   ↓
MaxPooling
   ↓
Conv2D
   ↓
Latent Space (Bottleneck)
   ↓
UpSampling
   ↓
Conv2D
   ↓
Output (Denoised Image)
```

---


## 📊 Performance Metrics

* **SSIM (Structural Similarity Index): ~0.75**
* Indicates moderate reconstruction quality
* Demonstrates effective noise reduction using hybrid model

---

## 🧰 Tech Stack

| Category      | Tools             |
| ------------- | ----------------- |
| Programming   | Python            |
| Libraries     | NumPy, OpenCV     |
| Deep Learning | TensorFlow, Keras |
| Visualization | Matplotlib        |

---

## 📂 Project Structure

```
ai-image-denoising-dsp-autoencoder/
│
├── notebook/
│     └── denoising.ipynb
│
├── outputs/
│     └── result_images/
│
├── images/
│     ├── original.png
│     ├── noisy.png
│     ├── denoised.png
│
├── report/
│     └── project_report.pdf
│
├── requirements.txt
└── README.md
```

---

## 📌 Applications

* 🏥 Medical Imaging (MRI, CT)
* 🛰️ Satellite Image Processing
* 🎥 Image Restoration Systems
* 🤖 Computer Vision Pipelines

---

## 🔮 Future Improvements

* Improve SSIM (>0.9) with deeper networks
* Add PSNR & MSE evaluation
* Implement real-time denoising
* Deploy using Flask / Web App

---

## 👨‍💻 Contributor@

* Sounak Maiti

---

## ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub!
