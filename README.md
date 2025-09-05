# Week 2: Sustainable Agriculture - Crop Recommendation Project

## 📌 Project Overview
This project predicts the most suitable crop for cultivation based on soil and environmental parameters like Nitrogen (N), Phosphorus (P), Potassium (K), temperature, humidity, pH, and rainfall. It uses machine learning models to recommend crops and provides insights via visualizations.

---

## 🗂 Dataset
- **Dataset Name:** Crop Recommendation Dataset
- **File:** `Crop_recommendation.csv`
- **Source:** [Kaggle](https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset)
- **Features:**
  - Nitrogen (N)
  - Phosphorus (P)
  - Potassium (K)
  - Temperature
  - Humidity
  - pH
  - Rainfall
  - Label (Crop Name)

---

## 🛠 Methodology
1. **Data Preprocessing**
   - Handled missing values (if any)
   - Label encoding for categorical target variable
2. **Exploratory Data Analysis (EDA)**
   - Visualizations: countplots, correlation heatmaps
   - Insights into crop distribution and feature correlations
3. **Model Building**
   - Logistic Regression
   - Decision Tree Classifier
   - Random Forest Classifier
4. **Model Evaluation**
   - Accuracy Score
   - Classification Report
   - Confusion Matrix
   - Random Forest achieved the best performance

---

## 🌱 Sample Prediction
```python
# Sample input: [N, P, K, temperature, humidity, pH, rainfall]
sample = np.array([[90, 42, 43, 20, 82, 6.5, 202]])
pred_crop = le.inverse_transform(rf_model.predict(sample))
print("Recommended Crop:", pred_crop[0])
