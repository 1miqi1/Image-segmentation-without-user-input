
# Image Segmentation Without User Input

## Overview

In this project, I designed, implemented, and evaluated a **two-stage computer vision pipeline** for **image segmentation without user input**:

1. **Grad-CAM (Gradient-weighted Class Activation Mapping)** – generates saliency maps highlighting image regions most relevant to a classifier’s prediction.
2. **Automatic segmentation using SAM (Segment Anything Model)** – segments objects using only the image input by automatically generating foreground and background point prompts.

This project focuses on **model interpretability** and **prompt-free image segmentation**, combining explanation methods with foundation models in a multi-stage pipeline.

---

## **Colab Notebook**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/1miqi1/Image-segmentation-without-user-input/blob/main/hw_2_gradcam_and_sam_student.ipynb)


*(I recommend using Colab)*

For fast replication, open the ready-to-run Colab version of the project.

The Colab version:

* Downloads the dataset
* Loads the pretrained classifier and SAM
* Computes Grad-CAM heatmaps
* Runs two segmentation pipelines
* Computes all evaluation metrics
* Generates visualizations
* Runs end-to-end without manual interaction

---

## **Runtime & Resource Requirements**

### **Hardware**

* **GPU strongly recommended**
* Verified on:

  * **Google Colab T4 GPU (16 GB RAM)**

### **Approximate Runtime**

| Stage                                  | Duration (Colab T4) |
| -------------------------------------- | ------------------- |
| Dataset download & setup               | ~10 seconds         |
| Model loading                          | ~10 seconds         |
| Grad-CAM computation                   | ~10 seconds         |
| SAM pipeline (foreground only)         | ~3–5 minutes        |
| SAM pipeline (foreground + background) | ~3-5 minutes        |

**Total runtime:**
**~6–10 minutes end-to-end**

### **Memory footprint**

* Dataset: **small (CIFAR-10-based)**
* SAM model: **~2–3 GB GPU RAM**
* Overall GPU usage: **fits within Colab T4 limits**

---

