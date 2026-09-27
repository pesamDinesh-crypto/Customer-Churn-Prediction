📊 Telco Customer Churn Prediction

A Machine Learning-based Telco Customer Churn Prediction project built using Python, Scikit-learn, Pandas, NumPy, and Tkinter.

The project predicts whether a telecom customer is likely to Churn or Not Churn based on customer information such as tenure, monthly charges, total charges, gender, and contract type.

🚀 Project Overview

Customer churn is an important problem for telecom companies. Predicting customers who are likely to leave can help businesses take appropriate actions to improve customer retention.

This project uses a Logistic Regression machine learning model to classify customers into:

✅ No Churn
⚠️ Churn

A simple Tkinter GUI is included so users can enter customer details and receive a churn prediction.

🛠️ Technologies Used
Python
Pandas
NumPy
Scikit-learn
Tkinter
LabelEncoder
StandardScaler
Logistic Regression
📁 Dataset

The project uses:

Telco-Customer-Churn.csv

The dataset contains telecom customer information including customer demographics, services, contract details, and churn status.

Important columns used in the project
customerID
gender
Partner
Dependents
PhoneService
MultipleLines
InternetService
OnlineSecurity
OnlineBackup
DeviceProtection
TechSupport
StreamingTV
StreamingMovies
Contract
PaperlessBilling
PaymentMethod
tenure
MonthlyCharges
TotalCharges
Churn
🔄 Machine Learning Workflow
Dataset
   ↓
Data Loading
   ↓
Data Preprocessing
   ↓
Handle Missing TotalCharges
   ↓
Categorical Encoding
   ↓
Train/Test Split
   ↓
Feature Scaling
   ↓
Logistic Regression
   ↓
Model Prediction
   ↓
Tkinter GUI
   ↓
Churn / No Churn
🧹 Data Preprocessing
1. Load Dataset

The dataset is loaded using Pandas:

dataset = pd.read_csv("Telco-Customer-Churn.csv")
2. Convert TotalCharges

TotalCharges is converted into numeric format and missing values are replaced with the median:

dataset['TotalCharges'] = pd.to_numeric(
    dataset['TotalCharges'],
    errors='coerce'
)

dataset['TotalCharges'] = dataset['TotalCharges'].fillna(
    dataset['TotalCharges'].median()
)
3. Encode Categorical Variables

Categorical columns are converted into numerical values using LabelEncoder.

le = LabelEncoder()
dataset[col] = le.fit_transform(dataset[col])
4. Train/Test Split

The dataset is divided into training and testing sets:

X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=0
)
5. Feature Scaling

StandardScaler is used to scale the features:

scaler = StandardScaler()

X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)
🤖 Machine Learning Model

The project uses Logistic Regression for binary classification.

model = LogisticRegression(max_iter=1000)
model.fit(X_train, y_train)

The model predicts whether the customer will churn.

prediction = model.predict(final_input)

The project also calculates the predicted churn probability:

prob = model.predict_proba(final_input)[0][1]
🖥️ Tkinter GUI

The project includes a graphical user interface created using Tkinter.

The user can enter:

Tenure
Monthly Charges
Total Charges
Gender
Contract Type

Then click:

Predict Churn

The application displays the prediction and probability.

Example:

Prediction: Churn
Probability: 0.72

or

Prediction: No Churn
Probability: 0.18
📸 Project Features
🔹 Customer Input

Users can enter customer information through the GUI.

🔹 Churn Prediction

The trained Logistic Regression model predicts the customer's churn status.

🔹 Probability

The application also displays the probability associated with the churn prediction.

🔹 Error Handling

Invalid input is handled using Tkinter error messages.

⚙️ Installation

Clone the repository:

git clone https://github.com/your-username/your-repository-name.git

Navigate to the project folder:

cd your-repository-name

Install the required libraries:

pip install numpy pandas scikit-learn

Tkinter is normally included with Python on Windows. If it is missing from your Python installation, install the appropriate Tkinter package for your operating system.

▶️ How to Run

Make sure these files are in the same project directory:

📁 Telco-Customer-Churn-Prediction
│
├── 📄 churn_prediction.ipynb
├── 📄 Telco-Customer-Churn.csv
└── 📄 README.md

Open the notebook in Jupyter:

jupyter notebook

Then run the notebook cells.

The Tkinter application will open automatically.

📊 Model Details
Component	Details
Problem	Customer Churn Prediction
Learning Type	Supervised Learning
Task	Binary Classification
Algorithm	Logistic Regression
Encoding	LabelEncoder
Scaling	StandardScaler
Test Size	20%
Random State	0
GUI	Tkinter
🎯 Project Objective

The main objective of this project is to develop a machine learning application that can:

Process telecom customer data.
Convert categorical data into numerical values.
Scale customer features.
Train a Logistic Regression model.
Predict customer churn.
Display the prediction through a user-friendly GUI.
💡 Future Improvements

The project can be further improved by adding:

Model accuracy and evaluation metrics
Confusion matrix
Precision, recall, and F1-score
Additional customer input fields
Better GUI design
Multiple machine learning algorithms
Feature importance analysis
Model saving using Joblib/Pickle
Web deployment using Flask or Streamlit
👨‍💻 Author

Pesam Dinesh

Python | Machine Learning | Data Analysis | Power BI | SQL

⭐ If You Like This Project

If you find this project useful, consider giving the repository a ⭐ on GitHub!

#Python #MachineLearning #DataScience #ScikitLearn #Pandas #NumPy #Tkinter #LogisticRegression #CustomerChurn #GitHub
