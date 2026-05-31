# satellite_vision_transfer

## Semantic segmentation with U-Net and Zero-Shot Testing
This Repo is a part of my summer research internship where i build this project. It contains a U-Net model for semantic segmentation. It was trained on Dubai Dataset (Kaggle dataset) using Google Colab. The model was fine-tuned and then tested on images from Mumbai where it had never seen data before (zero-shot testing). And then i gave around 50 images to the Decoder part of the U-Net model to make it learn amd finally tested it again on the entire Mumbai Dataset to calculate the IoU ((Intersection over Union) score. 

## Overview
The goal of this project is to test how severely does a semantic segmentation model degrade when trained on a highly planned metropolitian city and tested on a dense, unstructured city. And which classes suffer the most mismanagement.

Model: U-Net architecture.
Training Data: [Semantic segmentation of aerial imagery]. 
Environment: Trained on Google Colab (GPU). 
Testing: Validated on the original dataset and tested on new images from [Satellite Images Semantic Segmentation of Mumbai] to check if it works on unseen data. 

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
