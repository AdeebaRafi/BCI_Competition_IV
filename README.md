# Title: BCI Competition IV 2a - simple pipeline **

# Short description: 

This repository shows a simple pipeline to train a motor imagery classifier on the BCI Competition IV 2a dataset. For learning purpose, I train a model. The pipeline is simple and meant for learning. It uses MNE for data handling and CSP + LDA for classification.

# Files

notebook.ipynb: the notebook with code and notes

data/: place your .gdf files here (A01T.gdf, A02T.gdf, ...)

# What i did

Load raw .gdf EEG data using MNE

Bandpass filter 7-30 Hz

Extract epochs around event codes for motor imagery

Select left vs right hand trials for a binary task

Train CSP for spatial feature extraction and LDA for classification

Report test accuracy and show simple plots

# How to run

Install requirements: pip install mne scikit-learn matplotlib

Put a .gdf file in the data folder

Open the notebook or run the pipeline cell

# Results

On subject A04T the pipeline produced about 58 percent test accuracy on the left vs right task. This is a baseline number and can be improved.

# Why this approach

CSP + LDA is a standard baseline for motor imagery BCI work. It is fast and easy to interpret.

Using a simple pipeline helps learn the steps needed for EEG decoding before moving to deep models.

# Next steps

Try ICA for artifact removal

Try EEGNet for a deep learning baseline

Tune CSP components and classifier hyperparameters

Use cross validation and report average results
