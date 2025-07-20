## Predictive Modeling for Agriculture

This project uses machine learning to assist farmers in selecting the most suitable crop based on key soil components — **Nitrogen (N)**, **Phosphorous (P)**, **Potassium (K)**, and **pH**.\
The goal is to predict the best crop for a given set of soil metrics and evaluate which feature(s) are most predictive.

---

### Project Structure (Jupyter Notebook Sections)

1. **Importing Libraries**\
   All necessary Python libraries for data analysis, visualization, and modeling are imported.

2. **Data Loading and Inspection**\
   The dataset `soil_measures.csv` is loaded and explored for missing values, structure, and basic stats.

3. **Exploratory Data Analysis (EDA)**\
   Visual insights (e.g., `pairplot`, value counts, distributions) to understand soil attributes and class balance.

4. **Feature and Target Separation**\
   The soil features (`N`, `P`, `K`, `pH`) are separated from the target variable (`crop`).

5. **Train-Test Split**\
   Dataset split into training and test sets using `train_test_split`.

6. **Modeling: Logistic Regression with Pipeline**

   - A baseline logistic regression model is built using a `Pipeline` with `StandardScaler`.
   - A controlled experiment is done to find the **most predictive single soil component**.
   - Evaluation metrics: **F1-score**.

7. **Modeling: Random Forest with Pipeline**\
   A stronger ensemble model is built and evaluated similarly using the full feature set.
   - Evaluation metrics: **F1-score**, **Accuracy**, **Classification Report**, **Confusion Matrix**.

9. **(Additional) Predicting Best Crop for New Soil Data**\
   Predicts the most suitable crop based on custom soil input using the trained model.

10. **(Additional) Performance Comparison**\
   A side-by-side comparison of **Logistic Regression** and **Random Forest** using accuracy and F1 scores.

11. **Conclusion**\
    Summary of findings:

    - Best model based on test performance
    - Most predictive soil component

---

### Example Result

> **Final Model (Random Forest) Performance:**
>
> - Accuracy: `0.800`
> - Weighted F1-score: `0.798`

---

### Dataset

- `soil_measures.csv`: Contains soil component values (`N`, `P`, `K`, `pH`) and optimal crop labels.

---

### Dependencies

- Python 3.8+
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

Install with:

```bash
pip install -r requirements.txt
```

---

### Future Work

- Try other classifiers (e.g., XGBoost, SVM)
- Hyperparameter tuning
- PCA or t-SNE for dimension reduction 
- Add geolocation or weather features for better predictions
