# AIDI1002_Final_Project_GroupX_Laya_Prasanna
Final project for AIDI 1002 – out-of-scope-intent-detection-project
Group Members: Laya & Prasanna
Semester: Fall 2025

## Project Summary

This project reproduces the research paper on Out-of-Scope (OOS) Intent Detection using Contrastive Learning and BERT.
We successfully:

Loaded the same dataset from the paper

Reproduced the original model training process (BERT + contrastive loss)

Evaluated model performance on validation and test sets

### Our Contribution

We added a new model for experimentation:

- We extracted sentence embeddings (CLS token) from the trained BERT encoder and trained a Logistic Regression classifier to compare performance.

This provides insight into how well a linear classifier performs using pretrained BERT embeddings.

#### Logistic Regression Accuracy:

~70% on the test set

### Repository Structure
/src              – Original training and model files
/embeddings       – Contribution experiment (Logistic Regression)
/report           – Final project notebook and PDF
README.md

### Dataset

We used the same dataset included in the original paper’s repository (positive intents + OOS samples).
Data loading is handled automatically by the dataloader.

Running the Original Model
python main.py --loss_ce_only --num_train_epochs 1


This trains the BERT encoder and saves a checkpoint.

Note: The trained .pth model is large and stored separately in Google Drive.

**Model Checkpoint**

Because GitHub has file size limits, download:

bert_ce_epoch1.pth

Google Drive link: (add your link here)

Place inside:

/model

### Running Our Contribution

Open the notebook:

logistic_regression_experiment.ipynb


Run all cells to:

- Load trained encoder

- Extract embeddings

- Train logistic regression

- Evaluate accuracy

### Results Summary

Reproduced original method successfully

Logistic Regression achieved ~70% accuracy on extracted embeddings

Shows simple models can work effectively with BERT representations
