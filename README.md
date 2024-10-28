# SniffClassifier
ML code for classisfying respiratory patterns used in Johnson et al 2024


- Overview:
This experiment follows a process for classifying data using the k-NN algorithm with Dynamic Time Warping (KnnDtw) and compares results across different sample sizes and dataset balancing conditions.

- Experiment Setup:
Data: Total of 261 samples across four classes—OptoSniff (63), OdorSniff (65), BuzzSniff (63), and SpontaneousSniff (70).
Objective: Use KnnDtw to classify these samples, testing with 20, 40, and 60 samples per class. Results will be compared with F1 scores under different conditions:
Original dataset (63_65_63_70 samples).
Dataset balanced to 70 samples per class using SMOTE.

- Steps to Reproduce:
1) Open Notebook in Google Colab:
Open KNN_DTW_for_Classification.ipynb.
Run Initial Setup Cells.
Execute the first four cells to load necessary libraries and the DTW k-NN algorithm from the GitHub repository (https://github.com/markdregan/K-Nearest-Neighbors-with-Dynamic-Time-Warping).

2) Dataset Loading:
Update the dataset path in the cell to point to your specific Google Drive location of "SniffingData.xlsx".

3) Extract and Reshape Data:
Follow the comments to load values and reshape as required.

4) Run Classification for Various Sample Sizes:
Set "num_samples" to 20, 40, or 60 to select samples dynamically.
Skip cell with comment "# Train Test Split and Normalization for all samples (63_65_63_70)"
Split, normalize, and classify with KnnDtw for each sample size.

5) Run Classification on Full Dataset (63_65_63_70):
Use all samples from the original dataset without selecting specific sample sizes.
Run cell with comment "# Train Test Split and Normalization for all samples (63_65_63_70)"
Split, normalize, and classify with KnnDtw as per instructions.

6)Balanced Dataset with SMOTE:
Apply SMOTE to balance the dataset to 70 samples per class.
Split, normalize, and classify with KnnDtw on this balanced dataset.

7)Compare Results:
A graphical comparison of F1 scores for different scenarios: 20, 40, 60 samples, full original dataset, and SMOTE-balanced dataset.
