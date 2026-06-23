# Lite-π
## Induce to Empower: Improving Lightweight Baselines via Foundation Model Induction for Generalized Polyp Segmentation

<p align="center">
  <img src="figures/LitePi_Model.png" width="90%">
</p>

<p align="center">
  <b>🚀 Empowering lightweight segmentation networks through foundation model induction for robust cross-dataset generalization.</b>
</p>

---

## 📖 Introduction

Automated polyp segmentation remains a challenging task due to substantial appearance variations, indistinct polyp boundaries, and significant domain shifts across datasets.

While Vision Foundation Models (VFMs), such as **SAM**, **DINOv2**, and **OneFormer**, demonstrate remarkable generalization capabilities, their direct deployment for polyp segmentation is hindered by high computational demands and limited domain-specific annotations. Conversely, lightweight segmentation models, including **U-Net**, **U-Net++**, and **PraNet**, are computationally efficient but often suffer from poor cross-dataset generalization due to limited representational capacity.

To address this gap, we propose **Lite-π**, a novel **Foundation Model Induction (FMI)** framework that empowers lightweight segmentation baselines by inducing complementary semantic and structural knowledge from multiple foundation models.

---

## 💡 Our Approach: Lite-π

Lite-π consists of three key components:

- **FM-Specific Prototype Generation:** Extracts representative semantic priors from multiple foundation models.
- **Reconstruction-Based Semantic Alignment:** Aligns lightweight features with the induced foundation model representations.
- **Transformer-Based Fusion:** Preserves complementary semantic and boundary information while highlighting polyp-relevant representations.

<p align="center">
  <img src="figures/LitePi-Overview.png" width="95%">
</p>

---

## ✨ Highlights

- ✅ Novel Foundation Model Induction framework.
- ✅ Enhances lightweight segmentation models without expensive fine-tuning.
- ✅ Leverages complementary knowledge from multiple vision foundation models.
- ✅ Superior cross-dataset generalization.
- ✅ Minimal computational overhead.
- ✅ Suitable for real-time clinical deployment.

---

## 📊 Results

### Seen Datasets
- Kvasir-SEG
- CVC-ClinicDB

<p align="center">
  <img src="figures/Qual_LIte" width="90%">
</p>

### Unseen Datasets
- ColonDB
- CVC-300
- ETIS-LaribPolypDB

<p align="center">
  <img src="figures/LitePi-Unseen.png" width="90%">
</p>

Lite-π consistently improves lightweight baselines and achieves superior generalization performance on unseen datasets while maintaining computational efficiency.

---

## 📂 Repository Structure

```text
Lite-Pi/
├── datasets/
├── figures/
├── models/
├── foundation_models/
├── train.py
├── test.py
├── utils/
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/username/Lite-Pi.git
cd Lite-Pi
```

### Create Environment

```bash
conda create -n litepi python=3.10
conda activate litepi
pip install -r requirements.txt
```

---

## 📁 Dataset Preparation

```text
datasets/
├── Kvasir-SEG/
├── CVC-ClinicDB/
├── ColonDB/
├── CVC-300/
└── ETIS-LaribPolypDB/
```

---

## 🚀 Training

```bash
python train.py --model unet --dataset Kvasir --epochs 100
```

---

## 🧪 Testing

```bash
python test.py --model lite_pi --weights checkpoints/best.pth
```

---

## 📈 Performance

| Method | Params (M) | Kvasir | ClinicDB | ColonDB | CVC-300 | ETIS |
|--------|------------|---------|-----------|----------|----------|------|
| U-Net | - | - | - | - | - | - |
| U-Net++ | - | - | - | - | - | - |
| PraNet | - | - | - | - | - | - |
| Lite-π | - | **-** | **-** | **-** | **-** | **-** |

---

## 📎 Citation

```bibtex
@article{litepi2026,
  title={Induce to Empower: Improving Lightweight Baselines via Foundation Model Induction for Generalized Polyp Segmentation},
  author={Anonymous Authors},
  journal={Under Review},
  year={2026}
}
```

---

## 🙏 Acknowledgements

This repository builds upon several excellent open-source projects, including:

- Segment Anything Model (SAM)
- DINOv2
- OneFormer
- U-Net
- U-Net++
- PraNet

We thank the authors for making their code publicly available.
