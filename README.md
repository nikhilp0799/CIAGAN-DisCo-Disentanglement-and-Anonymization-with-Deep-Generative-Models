# 🔍 CIAGAN & DisCo: Disentanglement and Anonymization with Deep Generative Models

Welcome to our project repository for **CIAGAN** (Conditional Identity Anonymization GAN) and **DisCo** (Disentanglement via Contrastive Learning). This repository contains our full implementation pipeline, datasets, and supporting materials used for our graduate Data Science class project.

---

## 📁 Repository Structure

```
├── CIAGAN/
│   ├── Data_Science_Project_CIAGANPaper.ipynb   # Landmark extraction + CIAGAN model
│   ├── README_CIAGAN.md                          # Overview and progress of CIAGAN
│   └── assets/                                   # Optional - sample outputs or figures
│
├── DisCo/
│   ├── Data_Science_Project_DiscoPaper.ipynb    # Full DisCo model implementation
│   ├── README_DisCo.md                           # Overview and progress of DisCo
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
- Based on **CVPR 2020** paper.
- Uses **landmark + masked background + identity vector** to generate anonymized but realistic faces.
- Useful in preserving privacy while keeping usability for detection/tracking.
- We implemented:
  - Landmark extraction using `face_alignment` and CelebA
  - CIAGAN generator architecture
  - Dual discriminators: Real/Fake and Identity
  - Identity vector injection and loss

⚠️ Due to compute limits, model training was **not executed**. However, all core model components and data pipeline are in place.

---

### 🧬 DisCo: Disentangled Representation Learning
- Based on **ICLR 2022** paper.
- Uses **contrastive learning** to disentangle semantic factors in images using pretrained GANs.
- Highlights:
  - Navigator module to find latent directions
  - ∆-Contrastor architecture with variation space
  - Fully working encoder + loss pipeline
  - State-of-the-art performance on FFHQ & Shapes3D (in paper)

✅ We replicated the DisCo training pipeline successfully.

---

## 🚀 How to Run

### 🔧 Setup
```bash
pip install -r requirements.txt
```

Make sure your dataset structure is:
```
data/
├── CelebA/
│   ├── imgs/               # Original CelebA images
│   ├── landmarks_fan/      # Landmarks extracted using face_alignment
│   └── masks/              # Background masks (optional)
```

---

## 📊 Results & Visuals
- Sample landmark images and model architecture screenshots are included in the notebooks.
- DisCo outputs show disentangled changes in pose, hair, lighting direction.

---

## 🧾 Citations
- DisCo: [Disentanglement via Contrast (ICLR 2022)](https://github.com/xrenaa/DisCo)
- CIAGAN: [CIAGAN (CVPR 2020)](https://openaccess.thecvf.com/content_CVPR_2020/html/Maximov_CIAGAN_Conditional_Identity_Anonymization_Generative_Adversarial_Networks_CVPR_2020_paper.html)

---

## 👥 Contributors
- Ayush Patil, Nikhil Pandey,Kallem Harsha Vardhan Reddy, Northeastern University, MS in Information Systems (2025)

---

## 📌 License
This project is for academic and educational purposes only.

