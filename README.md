# Salary Prediction at Age 30

This project predicts the **expected salary at 30 years of age** based on a person’s **skills and other features** using a **Linear Regression model**.  

It is a beginner-friendly project demonstrating **data preprocessing, feature encoding, visualization, and regression modeling** in Python.

---

## Dataset

The dataset contains information about individuals’ skills and their salaries at 30. Key points:

- `Skills` – a list of skills for each person (e.g., Python, Java, Excel)  
- `Salary_at_30` – the salary of the person at 30 years old  
- Other features may include demographic or professional data.  

The dataset was loaded using `pandas` and processed for modeling.

---

## Data Preprocessing

1. **Drop unnecessary columns:** Removed columns like `Unnamed: 0` which are not useful.  
2. **Convert skills to usable format:** Skills were stored as strings; converted them into lists using `ast.literal_eval`.  
3. **One-hot encoding of skills:** Used `MultiLabelBinarizer` to convert skills into binary columns (1 = person has the skill, 0 = person does not).  
4. **Feature scaling:** Applied `StandardScaler` to normalize features for better regression performance.  

---

## Exploratory Data Analysis (EDA)

- Visualized **relationship between salary and each feature** using scatter plots.  
- Calculated **correlation of features with Salary_at_30** to identify important predictors.  

---

## Model

- **Model used:** Linear Regression (`sklearn.linear_model.LinearRegression`)  
- **Train-test split:** 70% train, 30% test  
- **Training:** Model trained on scaled feature data.  

---

## Evaluation Metrics

The model’s performance was evaluated using common regression metrics:

| Metric | Value |
|--------|-------|
| R² Score | 0.88 ✅ |
| Mean Absolute Error (MAE) | 3,928.81 |
| Mean Squared Error (MSE) | 23,666,511.37 |
| Root Mean Squared Error (RMSE) | 4,864.82 |

**Interpretation:**  
- The R² score of **0.88** means the model explains 88% of the variance in salaries — a strong prediction.  
- The MAE shows that on average, predictions differ from actual salaries by ~3,900.  
- RMSE is around 4,800, indicating a reasonable prediction error for salary in absolute terms.  

---

## Visualization

The project includes **scatter plots** showing how each feature affects the salary. This helps to **understand relationships between skills and salary**.

---

## How to Run

1. Install required packages:  

    pip install pandas numpy seaborn matplotlib scikit-learn

2. Load the dataset and run the script:

    python salary_prediction.py

3. The script will:

    - Preprocess data
    - Visualize relationships
    - Train a Linear Regression model
    - Print evalutaion metrics

---

## Conclusion

This beginner-friendly project demonstrates:

- How to handle list-based categorical features (skills) using one-hot encoding.
- How to scale features and train a regression model.
- How to evaluate model performance using R², MAE, MSE, and RMSE.

With an R² of 0.88, this model is capable of predicting salaries quite accurately based on skills.
