# satellite_vision_transfer

## Semantic segmentation with U-Net and Zero-Shot Testing
This Repo is a part of my summer research internship where i build this project. It contains a U-Net model for semantic segmentation. It was trained on Dubai Dataset (Kaggle dataset) using Google Colab. The model was fine-tuned and then tested on images from Mumbai where it had never seen data before (zero-shot testing). And then i gave around 50 images to the Decoder part of the U-Net model to make it learn amd finally tested it again on the entire Mumbai Dataset to calculate the IoU ((Intersection over Union) score. 

## Overview
The goal of this project is to test how severely does a semantic segmentation model degrade when trained on a highly planned metropolitian city and tested on a dense, unstructured city. And which classes suffer the most mismanagement. Then freeze the encoder part of the U-Net and train the model on 50 Mumbai Dataset and then finally check that the average (mIoU) is somewhere around the average (mIoU) of the planned metropolitian city.

Model: U-Net architecture.
Training Data: [Semantic segmentation of aerial imagery]. 
Environment: Trained on Google Colab (GPU). 
Testing: Validated on the original dataset and tested on new images from [Satellite Images Semantic Segmentation of Mumbai] to check if it works on unseen data. And finally check that the average (mIoU) is somewhere around the average (mIoU) when the model was tested on the planned metropolitian city data.

## Features
U-Net Architecture: Uses a standard encoder-decoder structure with skip connections for precise segmentation.
Fine-Tuning: The model was pre-trained and then fine-tuned on the specific Kaggle dataset for better accuracy.
Zero-Shot Capability: Successfully segments objects in images from locations not included in the training data. 
Few-shot training: Gives the score similar to the metro politian city data.
Easy Inference: Simple script to run predictions on new images. 
Colab Ready: Code is structured to run easily in Google Colab notebooks.

Results
The model performs well on the test set, shows good generalization on new images and after doing the few-shot training gives the result as good as it gave for the dubai dataset.

Test Type	Description	Performance
Validation	Images from the Kaggle dataset	[]
Zero-Shot	Images from [Insert New Location]	Visual Success (Segments objects correctly without retraining)

# Satellite Imagery — Semantic Segmentation

[![Open in nbviewer](https://img.shields.io/badge/Jupyter-Open%20in%20nbviewer-orange?logo=jupyter)](https://nbviewer.org/github/Aradhyay/satellite_vision_transfer/blob/main/Satellite_Imagery_GITHUB_READY%20(1).ipynb)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Aradhyay/satellite_vision_transfer/blob/main/Satellite_Imagery_GITHUB_READY%20(1).ipynb)
