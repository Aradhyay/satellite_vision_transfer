# Satellite Vision Transfer: Geographical Domain Shift

## Overview
This repository contains my summer research internship project. It explores how severely a semantic segmentation model degrades when trained on a highly planned, arid city (Dubai) and tested on a dense, subtropical city (Mumbai). And to also see that which classes suffer the most. 

Instead of retraining the entire model from scratch, I implemented an efficient **Few-Shot Fine-Tuning** strategy. In this stratergy i frooze the model's structural encoder part and training only its decoder part on just 50 local images, the model successfully adapted to the new geographical region.

## The Experiment Workflow
1. **Source Baseline:** Trained a U-Net model on the Dubai Kaggle Dataset.
2. **Source Prediction Result:** Noted the result score of the Predictions for future comparisons.
3. **Zero-Shot Testing (Domain Shift):** Tested the Dubai model directly on unseen Mumbai images. The model experienced a catastrophic drop in accuracy due to the drastic change in landscape, colors, and building density.
4. **Few-Shot Fine-Tuning:** Froze the U-Net's ResNet-34 encoder part. Extracted just 50 images from the Mumbai dataset to train *only* the decoder part of the model to recognize local textures.
5. **Final Evaluation:** Tested the fine-tuned model on the remaining 841 completely unseen Mumbai images and notedd the prediction result.
6. **Final Comparison:** Compared the *Source Prediction Result* and the Final Evaluation Result*.

## Features & Tech Stack
* **Architecture:** U-Net with a ResNet-34 Encoder (built with PyTorch).
* **Fine-Tuning Efficiency:** Recovers lost accuracy using minimal local data and compute power.
* **Classes Detected:** Unlabeled, Building, Land, Road, Vegetation, Water.
* **Colab Ready:** The code is structured to run directly in Google Colab notebooks.

## Results
The experiment proved that standard deep learning models suffer heavily under geographical domain shifts. However, fine-tuning just the decoder on a tiny local dataset successfully recovers—and even surpasses—the model's original baseline accuracy. You can see the images for more clarity.

| Phase | Dataset | Average Score (mIoU) | Description |
| :--- | :--- | :--- | :--- |
| **Baseline** | Dubai (Source) | **~0.62** | Strong initial segmentation on planned grids. |
| **Zero-Shot** | Mumbai (Target) | **~0.07** | Accuracy collapsed on new textures (Roads and Land dropped to near zero). |
| **Few-Shot** | Mumbai (Target) | **~0.70** | Recovered and surpassed the original baseline using only 50 local training images! |

## Images 
<img width="696" height="231" alt="Screenshot 2026-05-31 162842" src="https://github.com/user-attachments/assets/93edb5a6-80bc-4158-bd0b-3eabd39666d7" />
<img width="715" height="324" alt="Screenshot 2026-05-31 162956" src="https://github.com/user-attachments/assets/4246b1f0-c308-4814-beca-04e9081182f4" />
<img width="728" height="352" alt="Screenshot 2026-05-31 163039" src="https://github.com/user-attachments/assets/63d0a98b-7927-4fa8-a8c2-5fdd270aa259" />

## You can see my codes here
[![Open in nbviewer](https://img.shields.io/badge/Jupyter-Open%20in%20nbviewer-orange?logo=jupyter)](https://nbviewer.org/github/Aradhyay/satellite_vision_transfer/blob/main/Satellite_Imagery_GITHUB_READY%20(1).ipynb)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Aradhyay/satellite_vision_transfer/blob/main/Satellite_Imagery_GITHUB_READY%20(1).ipynb)
