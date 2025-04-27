# 🔍 CIAGAN & DisCo: Disentanglement and Anonymization with Deep Generative Models

Welcome to our project repository for **CIAGAN** (Conditional Identity Anonymization GAN) and **DisCo** (Disentanglement via Contrastive Learning).  
This repository contains our full implementation pipeline, datasets, and supporting materials developed for our graduate Data Science class project.

---

## 📁 Repository Structure

```
├── CIAGAN/
│   ├── Data_Science_Project_CIAGANPaper.ipynb   # Landmark extraction + CIAGAN model
│   ├── Dataset
│   
│
├── DisCo/
│   ├── Data_Science_Project_DiscoPaper.ipynb    # Full DisCo model implementation
│   
│
├── papers/
│   ├── CIAGAN_CVPR2020.pdf                      # Official CIAGAN paper
│   └── DisCo_ICLR2022.pdf                       # Official DisCo paper
│
├── requirements.txt                             # Dependencies
└── README.md                                     # This file
```

---

## 🧠 Project Overview

### 🎭 CIAGAN: Identity-Anonymized Face Generation
- Based on the **CVPR 2020** paper.
- Generates anonymized yet realistic face images using:
  - Facial landmarks
  - Masked background
  - Random identity control vector
- Key Implementations:
  - Landmark extraction using `face_alignment`
  - CIAGAN Generator and Dual Discriminator architecture
  - Identity vector injection for anonymization

⚠️ **Note:** Full model training was not completed due to compute limitations. However, architecture, data preparation, and loss functions are fully implemented.

---

### 🧬 DisCo: Disentangled Representation Learning
- Based on the **ICLR 2022** paper.
- Focuses on disentangling latent factors using **contrastive learning** without retraining the generator.
- Key Implementations:
  - Navigator for latent space exploration
  - ∆-Contrastor to capture semantic changes
  - Fully working Encoder and contrastive + entropy loss setup

 We replicated the DisCo training pipeline successfully using StyleGAN2 pretrained weights.

---

##  How to Reproduce

### 🔧 Setup
```bash
pip install -r requirements.txt
```

Ensure your dataset structure is organized as:
```
data/
├── CelebA/
│   ├── imgs/               # Original CelebA images
│   ├── landmarks_fan/      # Landmarks extracted using face_alignment
│   └── masks/              # Background masks (optional)
```

---

### ▶️ Running the Code

####  DisCo (Disentangled Representation Learning)
1. Open `DisCo/Data_Science_Project_DiscoPaper.ipynb`.
2. Make sure `stylegan2-ffhq-config-f.pkl` is downloaded (handled in the notebook).
3. Run all cells sequentially.
4. Training runs automatically; final visualizations show latent traversal and disentanglement.

####  CIAGAN (Conditional Identity Anonymization GAN)
1. Open `CIAGAN/Data_Science_Project_CIAGANPaper.ipynb`.
2. Run preprocessing cells to extract facial landmarks.
3. Setup Generator, Discriminators, and loss functions.
4. (Optional) Initiate training loop when sufficient compute is available.

---

##  Results & Visuals
- Included plots demonstrate:
  - For DisCo: Latent direction traversals and PCA visualizations.
  - For CIAGAN: Landmark extractions and embedding similarity (preliminary results).

---

##  Dependencies
- PyTorch
- Torchvision
- Face-alignment
- OpenCV
- Dlib
- Pillow
- Matplotlib
- Numpy
- tqdm
- scikit-image

(Automatically handled by `requirements.txt`)

---

##  Citations
- DisCo: [Disentanglement via Contrast (ICLR 2022)](https://github.com/xrenaa/DisCo)
- CIAGAN: [CIAGAN (CVPR 2020)](https://openaccess.thecvf.com/content_CVPR_2020/html/Maximov_CIAGAN_Conditional_Identity_Anonymization_Generative_Adversarial_Networks_CVPR_2020_paper.html)

---

## 👥 Contributors
- Ayush Patil
- Nikhil Pandey
- Harsha Vardhan Reddy Kallem

Northeastern University — MS in Information Systems, Class of 2025

---

##  License
This project is intended for academic and educational use only.

