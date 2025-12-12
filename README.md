# Breast Cancer Detection Using K-Means & KNN

Breast Cancer Detection Using K-Means and KNN Algorithms
The main focus of this project works on exploring and applying concepts from machine learning algorithms that would be useful for distinguishing benign from cancerous breast tissues. Based on the given Breast Cancer Wisconsin Dataset, it will undergo processing, clustering, and classification.

## Project Objectives

- Clean and prepare data for use with machine learning processes
- Encoding diagnosis labels as M = 1 and B = 0)
- Normalize Features with Min-Max Scaling
- Split Data set into train and test sets
- Use K-Means with k = 2 for clustering and finding patterns
- Create a KNN classifier with k = 5 for tumor classification
- Measure performance on accuracy, precision, recall, and F1-score metrics.


## Dataset Preprocessing

### 1. Encoding
The diagnosis values were given a numerical representation:

- Malignant (M) → 1  
- Benign (B) → 0

### 2. Column Cleaning
Eliminated unnecessary and empty columns:

- `id`  
- `Unnamed: 32`

### 3. Feature and Target Creation
- `y`: Diagnostics encoding label
- `X`: All remaining numerical feature columns

### 4. Scaling
Applied Min-Max normalization on all features.
It will result in better performance for K-Means and KNN.

### 5. Train–Test Split
- 80% training data  
- 20% testing data  
- Stratified sampling for maintaining class distribution.



## K-Means Clustering (k = 2)

K Means clustering algorithm was employed on the data to identify natural groups.

**Process:**
- Data grouped into 2 clusters
- Cluster labels vs. True diagnosis labels
- Cluster Purity computed

**Cluster Purity:** ~92%  
This central finding demonstrates that the natural clusters correspond very closely with the benign/malignant labels.


## KNN Classification with (k = 5)
The KNN algorithm was then trained on the scaled version of the training set and its performance measured on the testing set.
### KNN Model Performance
| Metric      | Score |
|-------------|--------|
| Accuracy    | ~96%   |
| Precision   | 1.00   |
| Recall      | ~0.90  |
| F1-Score    | ~0.95  |
The classifier performed well and managed to detect most cancerous instances, which was an excellent result for medical diagnosis. 

## Conclusion

It becomes clear from this project that simple models based on machine learning concepts can achieve remarkable and consistent performance on medical datasets with proper preprocessing. The main findings and conclusions include: 

- K-Means works well at identifying structure within data. 
- KNN shows high accuracy and excellent performance on detecting cancerous samples. 
- Encoding, scaling, and clean feature selection improve the performance.

As shown, the achieved results confirm once again that machine learning plays an essential role in assisting with early and correct detection related to breast cancer.
