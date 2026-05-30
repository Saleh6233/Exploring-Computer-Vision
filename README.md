# 👁️ Mastering Computer Vision Portfolio

Welcome to my Computer Vision repository! This portfolio documents my end-to-end journey mastering the landscape of computer vision, transitioning from foundational legacy architectures to state-of-the-art vision-language models.

The implementations in this repository are built using **Python, PyTorch, and OpenCV**.

---

## 🚀 Learning Roadmap

This repository is structured to reflect a rigorous deep learning curriculum. Checkmarks indicate completed or actively in-progress modules:

- [x] **Legacy CNNs** (Classification, Feature Extraction, ResNet, Inception)
- [ ] **Object Detection** (YOLO, SSD)
- [ ] **Image Segmentation** (U-Net, Mask R-CNN)
- [ ] **Generative AI** (GANs, VAEs)
- [ ] **Vision Transformers & Foundation Models** (ViT, SAM)

---

## 📁 Repository Structure

```text
Computer Vision/
├── Legacy CNNs/
│   └── master_cv_fine_tuning_resnet50.ipynb  <-- 🌟 Current Highlight
└── README.md
```

## 🎯 Project Highlights

### 1. ResNet-50 Transfer Learning & Hybrid LLM Reasoning Pipeline

**Directory:** `Legacy CNNs/`  
**Technologies:** PyTorch, Torchvision, DeepSeek API, Matplotlib, PIL

#### Project Overview

This project explores foundational transfer learning methodologies on a 5-class image classification task. To elevate the traditional pipeline, I developed a hybrid AI ecosystem combining a local computer vision model (ResNet-50) with cloud-based agentic LLM consultation using the DeepSeek API.

#### Key Implementations & Core Concepts Covered

- **Synthetic Data Prototyping:** Built data generation, preprocessing, and augmentation pipelines for image preparation.
- **Three Fine-Tuning Strategies Analyzed:**
  - **Feature Extraction:** Kept the entire ResNet-50 backbone frozen and trained only the final linear classifier layer.
  - **Partial Fine-Tuning:** Froze early layers and unfroze deep residual blocks (Layer 4) to capture domain-specific features.
  - **Full Fine-Tuning:** Trained the entire network with distinct, layer-wise learning rates to prevent catastrophic forgetting.
- **Agentic LLM Integration:** Connected the local training logs to DeepSeek's API, building an automated hyperparameter and architecture recommendation engine based on accuracy/compute trade-offs.

#### Key Takeaways & Visualizations

- Evaluated training dynamics across all three strategies via loss/accuracy charts.
- Demonstrated that while feature extraction is computationally inexpensive, partial and full fine-tuning can yield significantly better adaptation to domain-shifted data when proper learning-rate schedules are applied.

---

## ⚙️ Setup & Requirements

To run the notebooks locally, install the core dependencies:

```bash
pip install torch torchvision matplotlib pillow requests python-dotenv
```

For notebooks utilizing cloud-based reasoning, ensure you add your API credentials to a local `.env` file:

```env
DEEPSEEK_API_KEY=your_api_key_here
```

---

💡 This repository is under active development as I advance through my computer vision specializations. Feel free to explore the code, open issues, or connect with me!
