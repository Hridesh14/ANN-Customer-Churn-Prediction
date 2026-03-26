# Artificial Neural Network (ANN) - Customer Churn Prediction

## 📌 Project Overview
This project implements an Artificial Neural Network (ANN) to predict whether a bank customer will churn (leave the bank) or stay. By analyzing customer demographics and financial behaviors—such as credit score, geography, gender, age, tenure, and account balance—the model identifies high-risk customers, allowing the business to take proactive retention measures.

## 📊 Dataset
The dataset used for this project is typically `Churn_Modelling.csv`. It contains 10,000 rows of customer data with the following key features:
* **Inputs (Features):** CreditScore, Geography, Gender, Age, Tenure, Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary.
* **Output (Target):** Exited (1 = Churn, 0 = Retained).

*(Note: RowNumber, CustomerId, and Surname are dropped during preprocessing as they do not impact the prediction).*

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Deep Learning Framework:** TensorFlow / Keras
* **Data Manipulation:** Pandas, NumPy
* **Data Preprocessing & Evaluation:** Scikit-Learn (StandardScaler, train_test_split, accuracy_score, confusion_matrix)
* **Visualization:** Matplotlib / Seaborn

## 🧠 Model Architecture
The neural network is built using Keras' `Sequential` API with the following structure:
1. **Input Layer:** Accepts the 11 preprocessed and scaled features.
2. **Hidden Layers:** Dense layers utilizing the `ReLU` (Rectified Linear Unit) activation function to capture non-linear relationships. Weight initialization is done using `he_uniform` or `he_normal`.
3. **Dropout Layers:** Included to prevent overfitting during training.
4. **Output Layer:** A single Dense node utilizing the `Sigmoid` activation function to output a probability between 0 and 1.
5. **Compilation:** * Optimizer: `Adam`
   * Loss Function: `binary_crossentropy`
   * Metrics: `accuracy`

## 🚀 Installation and Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/ANN-Customer-Churn-Prediction.git](https://github.com/yourusername/ANN-Customer-Churn-Prediction.git)
   cd ANN-Customer-Churn-Prediction
Create a virtual environment (optional but recommended):

Bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
Install the required dependencies:

Bash
pip install -r requirements.txt
Run the model:

Bash
python ann.py
# Or open the Jupyter Notebook if you are using one:
# jupyter notebook
📈 Results
The model's performance is evaluated using a confusion matrix and an accuracy score. (You can update this section with your final accuracy score once you finish training the model, e.g., "The model achieved an accuracy of 86% on the test data.")

