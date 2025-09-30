#Model Used:# EEGNet - a specialized convolutional neural network designed for EEG signal classification Dataset: BCICIV_2a (Motor Imagery dataset) - left hand vs right hand classification Key Steps:
1. Loaded EEG data from GDF files using MNE
2. Preprocessed data (filtering 4-40 Hz, epoching)
3. Used only left hand (class 7) vs right hand (class 8) trials
4. Standardized the data
5. Trained EEGNet for 100 epochs with early stopping
6. Instead of just A01T, I will try multiple subjects
Why 59% is Problematic:
This is essentially random guessing (50% for binary classification), meaning model didn't learn meaningful patterns.
