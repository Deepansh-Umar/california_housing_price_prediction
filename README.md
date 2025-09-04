# 🏡 California Housing Price Prediction

This project predicts **median house values** in California districts using **Machine Learning**.  
The dataset contains housing, population, and income features, along with categorical location (`ocean_proximity`).  

---

## 📂 Dataset
We use the [California Housing Prices dataset](https://www.kaggle.com/datasets/camnugent/california-housing-prices).  
It includes the following columns:

- `longitude` – coordinate
- `latitude` – coordinate
- `housing_median_age` – median age of houses
- `total_rooms` – total number of rooms
- `total_bedrooms` – total number of bedrooms
- `population` – population in the district
- `households` – number of households
- `median_income` – median income of households
- `median_house_value` – target (house value in USD)
- `ocean_proximity` – categorical feature (e.g., `INLAND`, `NEAR BAY`, etc.)

---

## ⚙️ Steps Followed
1. **Data Loading & Exploration**
   - Checked dataset shape, missing values, and summary statistics.
   - Visualized distributions and correlations.
   
2. **Data Cleaning**
   - Handled missing values in `total_bedrooms` using median imputation.
   - Replaced/engineered new features such as:
     - `rooms_per_household`
     - `bedrooms_per_room`
     - `population_per_household`

3. **Feature Engineering**
   - Encoded categorical column `ocean_proximity` with one-hot encoding.
   - Scaled numerical features using `StandardScaler`.

4. **Model Training**
   - Split data into **train (80%)** and **test (20%)** sets.
   - Trained and compared models:
     - **Linear Regression**
     - **Decision Tree Regressor**
     - **Random Forest Regressor**

5. **Evaluation**
   - Used **Root Mean Squared Error (RMSE)** as the evaluation metric.
   - Compared performance of models.

---

## 📊 Results
- **Linear Regression** – baseline, interpretable but limited performance.
- **Decision Tree** – risk of overfitting, needs pruning/tuning.
- **Random Forest** – best performance, handles nonlinearities and categorical encoding well.

RMSE Scores:
- Linear Regression: 2.0312210391689993e-10
- Decision Tree: 101.44904709743086

---

## 🛠️ Tech Stack
- **Python**  
- **Pandas, NumPy** – Data manipulation  
- **Matplotlib, Seaborn** – Visualization  
- **Scikit-Learn** – ML models, pipelines, preprocessing  

---

## 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/Deepansh-Umar/california_housing_price_prediction.git
   cd california_housing_price_prediction
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook / Colab:

   ```bash
   jupyter notebook California_Housing_Price_Prediction.ipynb
   ```

   or open in [Google Colab](https://colab.research.google.com).

---

## 📌 Future Improvements

* Hyperparameter tuning with `GridSearchCV`.
* Try advanced models (XGBoost, Gradient Boosting, Neural Networks).
* Deploy as a **Flask/FastAPI web app** with an interactive frontend.
