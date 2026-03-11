**  Project Overview **  

Natural disasters such as floods cause significant damage to infrastructure, agriculture, and communities. Rapid identification of flooded areas is critical for disaster response teams to allocate resources efficiently and plan rescue operations.

This project focuses on semantic image segmentation using the U-Net architecture to automatically detect flooded regions in aerial imagery. The model performs pixel-level classification, distinguishing flooded areas from non-flooded terrain.

The goal of this project is to build a deep learning model capable of accurately identifying flood regions, which could assist emergency response teams and disaster management agencies.

Dataset

Dataset used in this project:

Flood Area Segmentation Dataset
Source: Kaggle

Dataset Link:
https://www.kaggle.com/datasets/faizalkarim/flood-area-segmentation

Dataset Characteristics

Property | Description
Images | ~290 aerial images
Resolution | ≥ 640×640
Classes | 2 (Flood, Background)
Task | Binary Image Segmentation

Challenges in the dataset include:

• Small dataset size
• Water reflections
• Muddy terrain that visually resembles flood water
• Class imbalance between flood and background regions

Repository Structure

learning-hub-flood-segmentation/

│
├── data/
│ └── dataset stored locally (not pushed to GitHub)
│

├── notebooks/
│ └── flood_area_segmentation.ipynb
│

├── src/
│ ├── data_loader.py
│ ├── augmentations.py
│ ├── model_unet.py
│ ├── losses.py
│ ├── train.py
│ ├── evaluate.py
│ └── visualization.py
│

├── outputs/
│ ├── figures/
│ │ ├── dataset_samples.png
│ │ ├── augmentation_examples.png
│ │ ├── unet_architecture.png
│ │ ├── training_curves.png
│ │ ├── prediction_examples.png
│ │ └── error_maps.png
│ │
│ └── metrics/
│ └── results_table.csv
│

├── models/
│ └── best_unet_model.h5
│

├── requirements.txt
├── .gitignore
├── README.md
└── report/
└── Learning_Hub_Report.pdf

Installation

Clone the repository

git clone https://github.com/your-repo/flood-segmentation.git

cd flood-segmentation

Install dependencies

pip install -r requirements.txt

Dataset Setup

Download the dataset from Kaggle:

https://www.kaggle.com/datasets/faizalkarim/flood-area-segmentation

Place the dataset inside the following directory:

data/flood_dataset/

Expected folder structure

data/
images/
masks/

Model Architecture

This project uses the U-Net architecture, a convolutional neural network designed specifically for image segmentation tasks.

The architecture consists of three main components:

Encoder (Contracting Path)
Extracts high-level image features through convolution and pooling layers.

Decoder (Expanding Path)
Upsamples feature maps to reconstruct spatial resolution.

Skip Connections
These connect encoder and decoder layers to preserve spatial information and improve segmentation accuracy.

Training Configuration

Parameter | Value
Model | U-Net
Image Resolution | 640×640
Epochs | 20
Batch Size | 8
Optimizer | Adam
Learning Rate | 0.001
Loss Function | Dice Loss + Binary Cross Entropy

Callbacks used during training:

• EarlyStopping
• ReduceLROnPlateau

Evaluation Metrics

The model performance was evaluated using the following metrics:

• Intersection over Union (IoU)
• Mean IoU (mIoU)
• Dice Coefficient

Example results

Class | IoU
Flood | 0.81
Background | 0.94

Mean IoU: 0.875
Dice Score: 0.89

Sample Predictions

The model generates the following outputs:

• Input aerial image
• Ground truth flood mask
• Predicted segmentation mask
• Error map highlighting incorrect predictions

Example outputs can be found in:

outputs/figures/

Team Contributions

Tanishq Rawat

• Model implementation
• Data preprocessing
• Training pipeline
• Model evaluation

Aristide Kanamugire

• Data augmentation
• Visualization
• Error analysis
• Report preparation

References

Flood Area Segmentation Dataset
https://www.kaggle.com/datasets/faizalkarim/flood-area-segmentation

Ronneberger, O., Fischer, P., Brox, T. (2015).
U-Net: Convolutional Networks for Biomedical Image Segmentation.
