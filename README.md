# 🩺 Diabetes Prediction: Data Analytics & Machine Learning

## 📖 Overview
This project explores a diabetes dataset to analyze health indicators and build a Machine Learning model capable of predicting diabetes based on clinical measurements. The project covers the full data pipeline: Exploratory Data Analysis (EDA), data cleaning, visualization, model building using TensorFlow, and performance evaluation.

## 📊 Dataset
*   **Target Variable:** Built using `glyhb >= 6.5` (indicating diabetes).
*   **Features Used:** `chol`, `stab.glu`, `hdl`, `ratio`, `age`, `height`, `weight`, `bp.1s`, `bp.1d`, `waist`, `hip`, and `time.ppn`.
*   **Dataset Size:** 390 rows.

## 🛠️ Tech Stack & Tools
*   **Language:** Python
*   **Data Analysis:** Pandas, NumPy
*   **Data Visualization:** Matplotlib, Seaborn
*   **Machine Learning:** TensorFlow, Scikit-Learn

## 🔍 Project Workflow

### 1. Data Cleaning & Preprocessing
*   **Missing Values:** Identified missing data and imputed it using the **training-set median** to prevent data leakage.
*   **Class Imbalance:** Addressed a significant class imbalance (only ~15% of the dataset represented diabetic patients).
*   **Feature Scaling:** Standardized numerical features for optimal neural network performance.

### 2. Exploratory Data Analysis (EDA)
*   Generated correlation matrices and distribution plots to understand feature relationships.
*   Created visualizations (histograms, box plots, and count plots) to analyze how features like `stab.glu`, `hdl`, and `ratio` differ between diabetic and non-diabetic patients.

### 3. Machine Learning Modeling
*   Built a Neural Network using **TensorFlow/Keras**.
*   Evaluated the model using a confusion matrix and classification report to generate the final results table.

## 📈 Results & Conclusion

**Performance:**
*   **Test Accuracy:** 85.9%
*   **Test Loss:** 0.82

**Key Takeaways:**
*   The network reached **85.9% test accuracy**, which is approximately the same as the ~85% majority-class baseline. Therefore, **recall on the diabetic class** is a much more important metric than overall accuracy for this specific problem.
*   The test loss of **0.82 is high**, suggesting the model is overconfident and overfitting the training data.

**Challenges Faced:**
*   **Small Dataset:** With only 390 rows, the model is prone to overfitting.
*   **Class Imbalance:** The dataset is heavily skewed (15% diabetic, 85% non-diabetic).
*   **Missing Data:** Required careful imputation to maintain data integrity.

**Future Improvements:**
To improve the model's robustness and predictive power, the following steps should be taken:
1.  **Handle Class Imbalance:** Implement class weights during training.
2.  **Reduce Overfitting:** Add Dropout layers and Early Stopping.
3.  **Hyperparameter Tuning:** Experiment with different numbers of layers and neurons.
4.  **Feature Engineering:** Include the categorical columns that were previously dropped.
5.  **Validation:** Implement K-Fold Cross-Validation to ensure the model's performance is consistent across different data subsets.

## 🚀 How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/diabetes-ml-project.git
