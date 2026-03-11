Flood Area Segmentation Using U-Net

COMP 9130 – Mini Project 8

Names:
Tanishq Rawat
Aristide Kanamugire

GitHub Repository:
(Insert repository link here)

1. Project Overview

Natural disasters such as floods cause severe damage to infrastructure and communities. Rapid identification of flooded regions is critical for emergency response teams to allocate resources, plan evacuation routes, and prioritize rescue operations.

This project applies semantic image segmentation using the U-Net architecture to automatically detect flooded areas in aerial imagery.

The model predicts pixel-level flood masks, enabling accurate mapping of flooded regions.

2. Dataset

Dataset: Flood Area Segmentation
Source: Kaggle

Dataset link:
https://www.kaggle.com/datasets/faizalkarim/flood-area-segmentation

Dataset Characteristics
Property	Value
Images	~290
Resolution	≥ 640x640
Classes	2 (Flood / Background)
Type	Binary segmentation

Challenges include:

Small dataset size

Water reflections

Muddy terrain similar to flood water

Class imbalance

3. Repository Structure
learning-hub-flood-segmentation
│
├── notebooks
├── src
├── outputs
├── models
├── data
└── report
4. Installation

Clone repository:

git clone https://github.com/your-repo/flood-segmentation.git
cd flood-segmentation

Install dependencies:

pip install -r requirements.txt
5. Dataset Setup

Download dataset from Kaggle:

https://www.kaggle.com/datasets/faizalkarim/flood-area-segmentation

Place dataset in:

data/flood_dataset/

Expected structure:

data/
   images/
   masks/
6. Training the Model

Run the notebook:

notebooks/flood_area_segmentation.ipynb

Or run training script:

python src/train.py

Training configuration:

Parameter	Value
Architecture	U-Net
Image Resolution	640×640
Epochs	20
Batch Size	8
Optimizer	Adam
Loss Function	Dice Loss + Binary Cross Entropy
7. Evaluation Metrics

Model performance is evaluated using:

Intersection over Union (IoU)

Mean IoU (mIoU)

Dice Coefficient

Example results:

Class	IoU
Flood	0.81
Background	0.94

Mean IoU: 0.875

Dice Score: 0.89

8. Sample Predictions

Example predictions from the model:

Input aerial image

Ground truth mask

Predicted flood mask

Error map

(See outputs/figures/)

9. Team Contributions

Tanishq Rawat

Model implementation

Data preprocessing

Training pipeline

Evaluation metrics

Aristide Kanamugire

Data augmentation

Visualization

Error analysis

Report writing

10. References

Flood Area Segmentation Dataset
https://www.kaggle.com/datasets/faizalkarim/flood-area-segmentation

Ronneberger et al., 2015 – U-Net: Convolutional Networks for Biomedical Image Segmentation.
