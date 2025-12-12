# Breast Cancer Detection Using K-Means & KNN

This project investigates how machine learning techniques can be applied to classify breast tumors as benign or malignant. Using the Breast Cancer Wisconsin Dataset, the workflow includes preprocessing, clustering, classification, and evaluation to measure how effectively machine learning models can support early cancer detection.



## Project Objectives

- Clean and prepare the dataset for machine learning workflows  
- Encode diagnosis labels (M = 1, B = 0)  
- Normalize features using Min-Max Scaling  
- Split data into training and testing subsets  
- Apply K-Means (k = 2) for clustering and pattern discovery  
- Train a KNN classifier (k = 5) for tumor classification  
- Evaluate performance using accuracy, precision, recall, and F1-score



## Dataset Preprocessing

### 1. Encoding
Diagnosis values were converted to numeric form:

- Malignant (M) → 1  
- Benign (B) → 0

### 2. Column Cleaning
Removed unnecessary or empty columns:

- `id`  
- `Unnamed: 32`

### 3. Feature and Target Creation
- `y`: Encoded diagnosis label  
- `X`: All remaining numerical feature columns

### 4. Scaling
Applied **Min-Max Normalization** to scale all features between 0 and 1.  
This ensures improved performance for both K-Means and KNN.

### 5. Train–Test Split
- 80% training data  
- 20% testing data  
- Stratified sampling to preserve class distribution.



## K-Means Clustering (k = 2)

K-Means clustering was used to explore natural groupings in the dataset.

**Process:**
- Data clustered into 2 groups  
- Cluster labels compared against true diagnosis labels  
- Cluster purity calculated

**Cluster Purity:** ~92%  
This shows that the natural clusters strongly align with the actual benign/malignant labels.



## KNN Classification (k = 5)

KNN was trained on the scaled training dataset and evaluated using the test set.

### KNN Model Performance
| Metric      | Score |
|-------------|--------|
| Accuracy    | ~96%   |
| Precision   | 1.00   |
| Recall      | ~0.90  |
| F1-Score    | ~0.95  |
The classifier demonstrated strong performance, accurately identifying most malignant cases—an important outcome in medical diagnostics.

## Conclusion

This project illustrates that even simple machine learning models can deliver strong and reliable performance on medical datasets when supported by proper preprocessing. Key conclusions include:

- K-Means effectively reveals underlying structure in the data.  
- KNN achieves high accuracy and performs well in identifying malignant cases.  
- Encoding, scaling, and clean feature selection significantly enhance model performance.

Overall, the results confirm the value of machine learning in supporting early and accurate breast cancer detection.
