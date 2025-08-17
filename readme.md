# Pneumonia Classification with ViT and CNN

This repository contains the code for the final project of the Reichman University Deep Learning course (Summer 2025). It implements and compares a Vision Transformer (ViT) and a CNN (ResNet-18) for classifying chest X-ray images as 'Normal' or 'Pneumonia'.


## 1. Data Setup

### Step 1: Download the Dataset
The project uses the "Chest X-Ray Images (Pneumonia)" dataset, which is publicly available on Kaggle.

* **Download Link:** [https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)

### Step 2: Set up the Directory Structure

After downloading and unzipping the dataset, you must place the data in a specific folder structure relative to the main project directory (where the notebook is located).

The required structure is:
```
Your-Project-Folder/
├── notebook.ipynb
├── chest_xray/
│   ├── train/
│   │   ├── NORMAL/
│   │   └── PNEUMIA/
│   ├── val/
│   │   ├── NORMAL/
│   │   └── PNEUMONIA/
│   └── test/
│       ├── NORMAL/
│       └── PNEUMONIA/
└── requirements.txt
```


## 2. Installation

To run this project, you need to install the required Python libraries.

### Step 1: Create a `requirements.txt` file
Create a file named `requirements.txt` in your main project folder and paste the following content into it:
```
torch
torchvision
numpy
pandas
matplotlib
timm
scikit-learn
torchmetrics
tqdm
```

### Step 2: Install the libraries
Open your terminal or command prompt, navigate to your project folder, and run the following command:
```bash
pip install -r requirements.txt
```

### 3. How to Run
---

The entire process is managed from a single Jupyter notebook.
### Step 1: Choose the Model to Run

Open the notebook and go to the cell containing the ProjectConfig class. Find the following line and set it to the model you wish to train and evaluate:
To run the Vision/CNN Transformer, set:
```
self.model_type = 'vit' or self.model_type = 'cnn'
```
### Step 2: Execute the Notebook
Run all the cells in the notebook sequentially from top to bottom.
The script will automatically:
1. Load the correct hyperparameters for the selected model.
2. Build the model architecture.
3. Train the model.
4. Display training graphs and the final evaluation results on the test set.

