# satellite_vision_transfer

## Semantic segmentation with U-Net and Zero-Shot Testing
This Repo is a part of my summer research internship where i build this project. It contains a U-Net model for semantic segmentation. It was trained on a Dubai Dataset (Kaggle dataset) using Google Colab. The model was fine-tuned and then tested on images from Mumbai where it had never seen data before (zero-shot testing).

## Overview
The goal of this project is to segment specific objects (like roads, buildings, or clouds) in images.

Model: U-Net architecture.
Training Data: [Insert Name of Kaggle Dataset]. 
Environment: Trained on Google Colab (GPU). 
Testing: Validated on the original dataset and tested on new images from [Insert Location Name] to check if it works on unseen data. 

## Features
U-Net Architecture: Uses a standard encoder-decoder structure with skip connections for precise segmentation.
Fine-Tuning: The model was pre-trained and then fine-tuned on the specific Kaggle dataset for better accuracy.
Zero-Shot Capability: Successfully segments objects in images from locations not included in the training data. 
Easy Inference: Simple script to run predictions on new images. 
Colab Ready: Code is structured to run easily in Google Colab notebooks.

Results
The model performs well on the test set and shows good generalization on new images. 

Test Type	Description	Performance
Validation	Images from the Kaggle dataset	[Insert IoU/Accuracy, e.g., 85% IoU]
Zero-Shot	Images from [Insert New Location]	Visual Success (Segments objects correctly without retraining)

This repo contains my summer research codes and results of exploring testing the geographical domain shift and few-shot fine-tuning in semantic segmentation.
