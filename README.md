# 🌾 Rice Yield Prediction Using Machine Learning

This project builds and compares multiple machine learning models to predict **rice yield** based on historical agricultural and climate data such as precipitation, temperature, area planted, and more. The model can help in planning, decision-making, and policy-making in the agriculture sector.

## 🛠️ Tools & Libraries
- Python
- Pandas, NumPy
- Scikit-learn (Preprocessing, Regression Models, Evaluation)
- Seaborn, Matplotlib (Data Visualization)
- Pickle (Model Deployment)

## 📂 Dataset
- Source: `final_rice_data1.xlsx` (contains yearly data by state including precipitation, temperature, production, planted and harvested area)
- Target variable: `yield`

## 🚀 ML Workflow

1. **Data Preprocessing**
   - Handled categorical features using `OneHotEncoder`
   - Scaled numerical features with `StandardScaler`

2. **Model Training & Comparison**
   - Linear Regression
   - Lasso Regression
   - Ridge Regression
   - Decision Tree Regressor (Best performance)
   - K-Nearest Neighbors

3. **Evaluation Metrics**
   - Mean Absolute Error (MAE)
   - R² Score

4. **Prediction Function**
   - Created a reusable `prediction()` function that takes new input and returns predicted rice yield.

5. **Model Saving**
   - Trained Decision Tree Regressor and Preprocessing Pipeline saved as `dtr.pkl` and `preprocessor.pkl`.

## 📊 Results

| Model            | MAE     | R² Score |
|------------------|---------|----------|
| Linear Regression | ~352.51 | 0.93     |
| Lasso             | ~353.81 | 0.93     |
| Ridge             | ~354.18 | 0.93     |
| Decision Tree     | ~312.67 | **0.94** |
| KNN               | ~391.23 | 0.91     |

## 🧠 Predicting Yield Example

```python
result = prediction(2005, 'Arkansas', 34.55, 64.09, 1643000)
print(f"Predicted Yield: {result}")
