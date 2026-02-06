# AI-ML-INTENSHIP-TASK--13
 PCA – Dimensionality Reduction
# PCA on MNIST Dataset with Logistic Regression

This project demonstrates **dimensionality reduction using Principal Component Analysis (PCA)** on the MNIST handwritten digits dataset and evaluates its impact on **Logistic Regression classification performance**. The goal is to reduce feature dimensionality while retaining most of the data variance and maintaining good classification accuracy.

---

##  Objectives

- Load MNIST digit images and labels
- Flatten images into feature vectors
- Scale features for effective PCA
- Apply PCA with different component counts
- Analyze explained variance
- Train Logistic Regression on reduced data
- Compare accuracy before and after PCA
- Visualize data in 2D PCA space

---

##  Dataset

- **MNIST Handwritten Digits Dataset**
- 28×28 grayscale images
- 10 digit classes (0–9)

Dataset files used (IDX format):
- `train-images.idx3-ubyte`
- `train-labels.idx1-ubyte`
- `t10k-images.idx3-ubyte`
- `t10k-labels.idx1-ubyte`

---

##  Libraries Used

- Python 3
- NumPy
- Matplotlib
- Scikit-learn

---

##  Project Workflow

### 1. Load Dataset
- MNIST images and labels are loaded from IDX files.
- Images are reshaped into `(28 × 28)` arrays.

### 2. Flatten Images
- Each image is converted into a **784-dimensional feature vector**.

### 3. Feature Scaling
- `StandardScaler` is applied to normalize features.
- Scaling is necessary for PCA to work correctly.

### 4. Apply PCA
- PCA is applied with different numbers of components:
  - 2
  - 10
  - 30
  - 50

### 5. Explained Variance Analysis
- Explained variance ratio is calculated for each PCA configuration.
- Cumulative variance plot is used to select optimal components.

### 6. Dimensionality Reduction
- Dataset is transformed using selected PCA components (e.g., 50).

### 7. Model Training
- Logistic Regression is trained:
  - On original scaled dataset
  - On PCA-reduced dataset

### 8. Model Evaluation
- Accuracy scores are compared between:
  - Original feature space
  - Reduced feature space

### 9. Visualization
- 2D PCA scatter plot is generated to observe digit separation.

---

##  Results

| Model | Feature Dimension | Accuracy |
|------|------------------|----------|
| Logistic Regression (Original) | 784 | High |
| Logistic Regression (PCA) | 50 | Slightly reduced but efficient |

- PCA significantly reduces dimensionality
- Model training becomes faster
- Accuracy remains competitive

---

##  Visualizations

- Cumulative explained variance vs number of components
- 2D PCA scatter plot showing digit clusters

---

##  Conclusion

- PCA effectively reduces dimensionality from **784 to 50**
- Most data variance is preserved
- Logistic Regression performs well even after reduction
- PCA improves computational efficiency with minimal accuracy loss

---

##  Future Improvements

- Try different classifiers (SVM, KNN)
- Tune Logistic Regression hyperparameters
- Experiment with more PCA components
- Add confusion matrix and classification report

---

##  Author

Developed as part of a Machine Learning dimensionality reduction experiment using the MNIST dataset.
