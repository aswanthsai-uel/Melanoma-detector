# Melanoma Detection using CNNs and Vision Transformers

## Overview

This project presents a comparative analysis of modern deep learning architectures for automated melanoma detection using dermoscopic skin lesion images. The study evaluates the performance of traditional Convolutional Neural Networks (CNNs) and Vision Transformers (ViTs) on the HAM10000 dataset.

The project compares:

* VGG19
* ResNet50
* Vision Transformer (ViT-B16)

Grad-CAM explainability was integrated to visualize model attention and improve interpretability of predictions.

---

## Dissertation Title

**FROM RESIDUAL NETWORKS TO VISION TRANSFORMERS: EVALUATING STATE-OF-THE-ART COMPUTER VISION MODELS FOR MELANOMA DETECTION**

---

## Objective

The objective of this work is to evaluate whether Vision Transformer architectures can outperform traditional CNN-based models for melanoma classification while maintaining clinically meaningful interpretability.

---

## Dataset

### HAM10000 Dataset

The project uses the HAM10000 ("Human Against Machine with 10,000") dermoscopic image dataset.

Dataset Link:

[HAM10000 Dataset](https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000?utm_source=chatgpt.com)

### Dataset Characteristics

* 10,015 dermoscopic images
* 7 skin lesion classes
* Significant class imbalance
* Real clinical dermatology images

---

## Models Evaluated

| Model    | Architecture Type  |
| -------- | ------------------ |
| VGG19    | Deep CNN           |
| ResNet50 | Residual CNN       |
| ViT-B16  | Vision Transformer |

---

## Methodology

The experimental pipeline includes:

1. Image preprocessing and resizing
2. Data augmentation
3. Transfer learning using ImageNet weights
4. Model training and evaluation
5. Grad-CAM explainability analysis
6. Comparative performance analysis

---

## Technologies Used

* Python
* PyTorch
* Torchvision
* TIMM
* Grad-CAM
* Scikit-learn
* Matplotlib
* Seaborn
* Google Colab

---

## Experimental Results

| Model    | Accuracy | Macro F1 Score | Melanoma Recall |
| -------- | -------- | -------------- | --------------- |
| VGG19    | 70.19%   | 0.2836         | 33.63%          |
| ResNet50 | 84.47%   | 0.7601         | 77.13%          |
| ViT-B16  | 86.82%   | 0.8041         | 70.40%          |

### Key Findings

* Vision Transformer achieved the best overall classification performance.
* ResNet50 achieved the highest melanoma recall.
* Grad-CAM visualizations showed clinically relevant lesion attention regions.

---

## Repository Structure

```text
Melanoma-detector/
│
├── melanoma_detection.ipynb
├── README.md
├── requirements.txt
├── saved_results/
│   ├── model_comparison_results.csv
│   ├── classification_reports.txt
│   ├── resnet50_model.pth
│   ├── vgg19_model.pth
│   └── vit_model.pth
│
├── sample_outputs/
│   ├── confusion_matrix_resnet50.png
│   ├── confusion_matrix_vgg19.png
│   ├── confusion_matrix_vit.png
│   ├── accuracy_comparison.png
│   ├── f1_comparison.png
│   └── gradcam_resnet50.png
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/aswanthsai-uel/Melanoma-detector.git
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Running the Project

Open the notebook:

```bash
melanoma_detection.ipynb
```

Run all cells sequentially in Google Colab or Jupyter Notebook.

---

## Explainability

Grad-CAM heatmaps were used to visualize model attention and verify whether predictions focused on clinically relevant lesion regions rather than background artifacts.

---

## Limitations

* Severe dataset imbalance
* Limited computational resources
* No external clinical dataset validation
* Models trained on curated dermoscopic images only

---

## Future Work

* Evaluate models on larger and more diverse dermatology datasets
* Explore hybrid CNN-Transformer architectures
* Integrate clinical metadata such as age and lesion location
* Improve model robustness for real-world noisy clinical images

---

## References

[1] A. Esteva et al., "Dermatologist-level classification of skin cancer with deep neural networks," *Nature*, vol. 542, pp. 115-118, 2017.

[2] A. Dosovitskiy et al., "An image is worth 16x16 words: Transformers for image recognition at scale," in *Proc. ICLR*, 2021.

[3] R. R. Selvaraju et al., "Grad-CAM: Visual explanations from deep networks via gradient-based localization," in *Proc. IEEE ICCV*, pp. 618-626, 2017.

[4] P. Tschandl et al., "The HAM10000 dataset: A large collection of multi-source dermatoscopic images of common pigmented skin lesions," *Scientific Data*, vol. 5, p. 180161, 2018.

[5] K. He, X. Zhang, S. Ren, and J. Sun, "Deep residual learning for image recognition," in *Proc. IEEE CVPR*, pp. 770-778, 2016.

[6] K. Simonyan and A. Zisserman, "Very deep convolutional networks for large-scale image recognition," in *Proc. ICLR*, 2015.

---

## Author

**Aswanth Sai Paleru**
MSc Computing
University of East London

---

## Academic Use

This repository was developed as part of an MSc dissertation project for academic and research purposes.
