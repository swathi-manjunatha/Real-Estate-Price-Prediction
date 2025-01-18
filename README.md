# Real Estate Price Prediction in Bengaluru Using Machine Learning

## Short Description
This project leverages machine learning techniques to predict house prices in Bengaluru, India, based on features like size, number of rooms, location, and bathrooms. It includes data preprocessing, feature engineering, outlier detection, and model evaluation to create a reliable price prediction system. The model was deployed as a Flask-based web application hosted on AWS EC2 with Nginx as a reverse proxy for production readiness.

---

## 1. Objective
This project aims to build a machine learning model to predict house prices in Bengaluru, India, based on features such as size, number of rooms, location, and bathrooms. The project involves data cleaning, preprocessing, outlier removal, feature engineering, and model evaluation to create an accurate and reliable price prediction system.

---

## 2. Dataset
- **Source:** Bengaluru House Price Dataset (collected from Kaggle:https://www.kaggle.com/datasets/amitabhajoy/bengaluru-house-price-data/data)
- **Size:** 13,000+ rows and multiple features like location, size, total_sqft, bath, and price.
- **Target Variable:** Price (in lakh Indian Rupees)

---

## 3. Tools and Technologies
- **Programming Languages:** Python
- **Libraries and Frameworks:** Pandas, NumPy, Matplotlib, Scikit-learn, Flask
- **Visualization Tools:** Matplotlib
- **Deployment:** Flask (web application)

---

## 4. Key Steps
### 4.1 Data Preprocessing
- Dropped irrelevant columns like 'area_type', 'availability', 'balcony', and 'society'.
- Handled missing values by dropping rows with null entries.
- Extracted numerical features like **BHK** from categorical columns.
- Processed inconsistent formats in square footage (e.g., ranges) by converting them into numerical averages.

### 4.2 Feature Engineering
- Created new features such as **price per square foot (PPS)** for better predictions.
- Applied **One-Hot Encoding** to handle categorical variables like location.
- Grouped less frequent locations into a single category labeled as 'other'.

### 4.3 Outlier Detection and Removal
- Removed entries where the price per square foot was statistically anomalous using **mean and standard deviation**.
- Eliminated unrealistic data points, such as very small apartments (<300 sqft per BHK).
- Addressed anomalies where the number of bathrooms exceeded the number of bedrooms by more than 2.

### 4.4 Model Building
- Implemented and tested multiple regression models:
  - **Linear Regression**
  - **Lasso Regression**
  - **Decision Tree Regressor**
- Used **GridSearchCV** to optimize hyperparameters and identify the best-performing model.
- Evaluated model performance using **R² score**, achieving an accuracy of approximately **83%**.

### 4.5 Model Deployment
- Developed a **Flask API** to serve the model predictions.
- Created routes to accept user input and return predicted prices dynamically.

---

## 5. Results and Insights
- Built a robust model to predict house prices based on key features like **location** and **size**.
- Identified the most influential variables affecting house prices.
- Provided visualization tools to analyze price distribution and location-wise trends.

---

## 6. Installation and Usage
### 6.1 Requirements
```
Python 3.x
pip install -r requirements.txt
```
### 6.2 How to Run
1. Clone the repository:
```
git clone <repository-link>
```
2. Navigate to the project folder:
```
cd House-Price-Prediction
```
3. Activate virtual environment (optional but recommended):
```
python3 -m venv venv
source venv/bin/activate
```
4. Install dependencies:
```
pip install -r requirements.txt
```
5. Run Flask server:
```
python server.py
```
6. Access the application in your browser:
```
http://127.0.0.1:5000/
```

---

## 7. Results
- **Model Accuracy:** ~83% on test data.
- **Key Feature Impact:** Location and size significantly influence pricing.

---

## 8. Repository Link
[GitHub Repository](<link-to-repository>)
  

