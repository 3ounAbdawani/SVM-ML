# SVM.ipynb: Support Vector Machine (SVM) Kernel Comparison

## 📋 Project Description
This Jupyter notebook, `SVM.ipynb`, demonstrates the application and comparison of **Support Vector Machine (SVM)** classifiers using four different kernel functions: **Linear**, **Polynomial**, **Radial Basis Function (RBF)**, and **Sigmoid**.

The purpose of this notebook is to:
* Load and prepare a well-known classification dataset.
* Implement various SVM models with different kernel functions.
* Standardize the features for optimal model performance.
* Evaluate the performance of each classifier using common metrics.
* Visualize the decision boundaries of each SVM kernel.

---

## 📊 Dataset
The notebook utilizes the **Iris dataset**, a classic multi-class classification problem. For the purpose of 2D visualization of the decision boundaries, only the first two features (`sepal length (cm)` and `sepal width (cm)`) are used for training and testing.

---

## 🛠️ Models and Methods
### Preprocessing
* **Data Split**: The dataset is split into training and testing sets with a `test_size` of **0.3** (30% for testing).
* **Scaling**: Features are scaled using the **StandardScaler** to normalize the data, which is crucial for distance-based algorithms like SVM.

### Classifiers Implemented
The following four SVM classifiers are trained and evaluated:

| Classifier Name | Kernel Type | Key Parameters |
| :--- | :--- | :--- |
| **Linear SVM** | `linear` | `C=1.0` |
| **Polynomial SVM** | `poly` | `degree=3`, `C=1.0` |
| **RBF SVM** | `rbf` | `gamma=0.7`, `C=1.0` |
| **Sigmoid SVM** | `sigmoid` | `gamma=0.1`, `C=1.0` |

### Evaluation Metrics
Each model is evaluated on the test set using the following metrics:
* **Accuracy Score**
* **Confusion Matrix**
* **Classification Report** (including Precision, Recall, and F1-Score)

---

## ✨ Results Summary
The performance metrics reported in the notebook for the test set show the following accuracies:

| Classifier | Accuracy |
| :--- | :--- |
| Linear SVM | 0.73 |
| Polynomial SVM | 0.76 |
| RBF SVM | 0.73 |
| **Sigmoid SVM** | **0.80** |

The **Sigmoid SVM** achieved the highest accuracy of 0.80 on the test data with the selected two features.

---

## 💻 Dependencies
To run this notebook successfully, you will need the following Python libraries. You can typically install them using `pip`:

```bash
pip install numpy matplotlib scikit-learn mlxtend
