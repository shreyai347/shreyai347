# 👋 Hello there!

Welcome to my GitHub profile! I'm **Shreya** ✨, a passionate data enthusiast eager to uncover insights and tell stories through data analysis.

## 🔍 About Me
- 👀 I’m interested in **Data Insights**: I love diving deep into datasets to extract meaningful patterns and trends. 📊
- 🌱 Currently learning in **Bangalore, Karnataka**: Exploring the tech hub of India while honing my data skills! 🚀
  
## 🛠️ Tech Stack
Here's a glimpse of the technologies I'm working with:
- 📈 **Data Science** 
- 🤖 **Machine Learning** 
- 🧠 **Deep Learning** 
- 🗣️ **NLP (Natural Language Processing)** 
- 🐍 **Python** 
- 🔍 **Exploratory Data Analysis (EDA)** 
- 🗄️ **SQL** 
- 📊 **Power BI** 
- 📝 **Jupyter/Google Colab** 
- 🌐 **Flask** 

## 🌟 Fun Fact
I believe data is like a treasure chest; the more you dig, the more you discover! 🏴‍☠️💎

## 📫 Let's Connect
I’d love to connect with fellow data enthusiasts, so feel free to reach out to me! 🤝

- ✉️ Email: [shreyashreya2322@gmail.com](mailto:shreyashreya2322@gmail.com)
- 🔗 LinkedIn: [Shreya Nagarbawdi](https://www.linkedin.com/in/shreya-nagarbawdi-a7749a24a/)

## ⚡ Fun Fact
When I'm not analyzing data,  I'm hanging out with friends ☕ and watching series!🏞️! 

Thank you for visiting my profile. Let's embark on this data journey together! 🎉














Here’s a breakdown of common machine learning algorithms and the key hyperparameters that are typically tuned to enhance performance:

### 1. **Linear Regression / Logistic Regression**
- **Key Hyperparameters:**
  - **`penalty`**: Type of regularization (e.g., `'l1'`, `'l2'`, `'elasticnet'`).
  - **`C`**: Inverse of regularization strength (smaller values for stronger regularization).
  - **`solver`**: Algorithm to use in optimization (e.g., `'lbfgs'`, `'liblinear'`).

  **Tuning Strategy**:
  - Choose the appropriate regularization type (`penalty`).
  - Adjust regularization strength (`C`).

---

### 2. **Decision Trees**
- **Key Hyperparameters:**
  - **`max_depth`**: Maximum depth of the tree to prevent overfitting.
  - **`min_samples_split`**: Minimum number of samples required to split a node.
  - **`min_samples_leaf`**: Minimum number of samples required in a leaf node.
  - **`max_features`**: Number of features to consider when splitting a node.

  **Tuning Strategy**:
  - Limit the depth (`max_depth`) to prevent overfitting.
  - Adjust `min_samples_split` and `min_samples_leaf` to generalize the tree.
  - Try different values of `max_features`.

---

### 3. **Random Forests**
- **Key Hyperparameters:**
  - **`n_estimators`**: Number of trees in the forest.
  - **`max_depth`**: Maximum depth of the tree.
  - **`min_samples_split`**: Minimum samples to split an internal node.
  - **`min_samples_leaf`**: Minimum samples in a leaf node.
  - **`max_features`**: Number of features to consider at each split.
  - **`bootstrap`**: Whether bootstrap samples are used when building trees.
  
  **Tuning Strategy**:
  - Increase the number of trees (`n_estimators`) for better accuracy.
  - Limit tree depth (`max_depth`) to prevent overfitting.
  - Tune `min_samples_split` and `min_samples_leaf` for better generalization.

---

### 4. **Support Vector Machines (SVM)**
- **Key Hyperparameters:**
  - **`C`**: Regularization parameter (higher values lead to less regularization).
  - **`kernel`**: Kernel type (e.g., `'linear'`, `'poly'`, `'rbf'`, `'sigmoid'`).
  - **`gamma`**: Kernel coefficient for non-linear kernels like RBF.
  
  **Tuning Strategy**:
  - Adjust `C` for regularization.
  - Choose a kernel that fits your data (e.g., `'rbf'` for non-linear).
  - Tune `gamma` for non-linear kernels.

---

### 5. **K-Nearest Neighbors (KNN)**
- **Key Hyperparameters:**
  - **`n_neighbors`**: Number of neighbors to use.
  - **`weights`**: How to weight the neighbors (e.g., `'uniform'`, `'distance'`).
  - **`p`**: Power parameter for the Minkowski distance (1 = Manhattan, 2 = Euclidean).

  **Tuning Strategy**:
  - Increase or decrease `n_neighbors` to find the best balance between underfitting and overfitting.
  - Use `distance` weighting for distance-based voting.
  - Experiment with the distance metric (`p`).

---

### 6. **Gradient Boosting / XGBoost**
- **Key Hyperparameters:**
  - **`n_estimators`**: Number of boosting rounds.
  - **`learning_rate`**: Shrinks the contribution of each tree.
  - **`max_depth`**: Maximum depth of individual trees.
  - **`subsample`**: Fraction of samples to use for fitting each tree.
  - **`colsample_bytree`**: Fraction of features to use at each tree split.
  
  **Tuning Strategy**:
  - Increase the number of trees (`n_estimators`) with a smaller `learning_rate`.
  - Control overfitting with `max_depth`, `subsample`, and `colsample_bytree`.

---

### 7. **Artificial Neural Networks (ANN)**
- **Key Hyperparameters:**
  - **`hidden_layer_sizes`**: Number and size of hidden layers.
  - **`activation`**: Activation function (e.g., `'relu'`, `'tanh'`).
  - **`alpha`**: Regularization term (L2 penalty).
  - **`learning_rate`**: Schedule for weight updates.
  - **`learning_rate_init`**: Initial learning rate.
  
  **Tuning Strategy**:
  - Adjust the number of hidden layers and neurons.
  - Try different activation functions.
  - Tune the learning rate (`learning_rate_init`).

---

### 8. **K-Means Clustering**
- **Key Hyperparameters:**
  - **`n_clusters`**: Number of clusters.
  - **`init`**: Initialization method for centroids (`'k-means++'` is recommended).
  - **`max_iter`**: Maximum number of iterations for the algorithm.
  
  **Tuning Strategy**:
  - Increase the number of clusters (`n_clusters`) based on the data.
  - Ensure proper centroid initialization with `init='k-means++'`.

---

### 9. **Principal Component Analysis (PCA)**
- **Key Hyperparameters:**
  - **`n_components`**: Number of principal components to keep.
  - **`svd_solver`**: Method for computing the decomposition.
  
  **Tuning Strategy**:
  - Choose the appropriate number of components (`n_components`) based on explained variance.
  - Use `'auto'` or `'full'` solvers depending on dataset size.

---

### 10. **Lasso / Ridge Regression**
- **Key Hyperparameters:**
  - **`alpha`**: Regularization strength (higher values mean more regularization).
  - **`max_iter`**: Maximum number of iterations for convergence.
  
  **Tuning Strategy**:
  - Adjust the `alpha` parameter for regularization.
  - Ensure convergence by tuning `max_iter`.

---

### 11. **LightGBM / CatBoost**
- **Key Hyperparameters:**
  - **`learning_rate`**: Step size shrinkage.
  - **`num_leaves`**: Number of leaves in one tree.
  - **`max_depth`**: Maximum depth of each tree.
  - **`n_estimators`**: Number of boosting rounds.

  **Tuning Strategy**:
  - Adjust `learning_rate` and increase `n_estimators`.
  - Use smaller `max_depth` and tune `num_leaves` for performance improvement.

---

By focusing on the above hyperparameters for each algorithm, you can significantly improve model performance through fine-tuning.
