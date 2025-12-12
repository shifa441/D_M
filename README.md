#Breast Cancer Detection Using K-Means & KNN

This project explores how machine learning can help distinguish between benign and malignant breast tumors.
Using the Breast Cancer Wisconsin Dataset, we preprocess the data, perform clustering, and build a classification model to evaluate how well machine learning can predict tumor types.

**Project Goals**

The main objectives of this project are:

To clean and prepare the dataset for machine learning

To encode the diagnosis labels (M = 1, B = 0)

To apply Min-Max normalization for consistent scaling

To split the dataset into training and testing sets

To use K-Means clustering (k=2) to observe natural patterns

To train a KNN classifier (k=5) to classify tumor types

To evaluate the model using accuracy, precision, recall, and F1-score

** Data Preprocessing**

To prepare the dataset:

**Encoding:**

Malignant (M) → 1

Benign (B) → 0

**Column Cleaning:**
We remove unnecessary columns such as:

id

Unnamed: 32

**Feature & Target Creation:**

y = diagnosis_encoded

X = all numeric feature columns

**Scaling:**

Applied Min-Max Scaling so all feature values fall between 0 and 1.

This improves the performance of both K-Means and KNN.

** Train–Test Split**

The dataset is divided into:

80% training data

20% testing data
With stratification to maintain the original class distribution.

** K-Means Clustering (k = 2)**

K-Means is used to identify natural groupings in the data.

It clusters the points into 2 groups

Then, we compare each cluster to the actual diagnosis labels

We calculate cluster purity, which indicates how well clusters represent real classes

** Cluster Purity: ≈ 92%**
This means the clusters were fairly consistent with the true labels.

**KNN Classification (k = 5)**

KNN is used to classify tumors based on their similarity to previous samples.

After training the model on the scaled training data, the test results were:

 **KNN Model Performance**

Accuracy: ~96%

Precision: 1.00

Recall: ~0.90

F1-Score: ~0.95

The model performed very well and correctly classified most malignant cases, which is very important in medical diagnosis.


** Conclusion**

This project highlights how machine learning can be applied to medical data to help with diagnosis.
Key takeaways:

K-Means gives a good overview of natural groupings in the dataset

KNN provides highly accurate classification results

Scaling and preprocessing have a significant impact on performance

Together, these techniques show how simple ML models can achieve strong results in health-related data analysis.
