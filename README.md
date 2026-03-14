# Mini Project 8: Flood Area Segmentation  
**COMP 9130 – Applied Artificial Intelligence**  
**Natural Disaster Damage Assessment**  

## Project Overview
Natural disasters such as floods cause significant damage to infrastructure, agriculture, and communities. Rapid identification of flooded areas is critical for disaster response teams to allocate resources efficiently and plan rescue operations.

This project applies **semantic segmentation** using the **U-Net architecture** to automatically detect flooded regions in aerial imagery at the pixel level. The model distinguishes flooded water from non-flooded terrain, supporting emergency response and disaster management.

**Goal**: Build a robust U-Net model (minimum 640×640 resolution) that achieves high mIoU on the Flood Area Segmentation dataset.
## Dataset
**Dataset used**: Flood Area Segmentation  
**Source**: Kaggle  
**Link**: [https://www.kaggle.com/datasets/faizalkarim/flood-area-segmentation](https://www.kaggle.com/datasets/faizalkarim/flood-area-segmentation)

**Characteristics**:
| Property       | Description                          |
|----------------|--------------------------------------|
| Images         | ~290 aerial/UAV images               |
| Resolution     | ≥ 640×640 pixels                     |
| Classes        | Binary (Flood / Background)          |
| Task           | Semantic Segmentation                |

**Challenges**:
- Small dataset size → requires strong augmentation
- Water reflections & muddy areas create visual ambiguity
- Class imbalance

**Business Context**: Emergency response teams need rapid flood mapping to prioritize rescue operations and allocate resources.
## Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/aristidekanamugire/Mini-Project-8.git
cd Mini-Project-8
pip install -r requirements.txt
3. Download the dataset

Go to: Kaggle Flood Area Segmentation
Download and extract into:text
