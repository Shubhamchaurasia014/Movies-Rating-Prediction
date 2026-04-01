# 🎬 MovieLens Ratings Prediction

## 📌 Project Overview
This project uses the **MovieLens dataset** to build machine learning models that predict user ratings for movies. The dataset contains information about movies, users, and ratings.

The goal is to build ML models and evaluate their performance using metrics like **RMSE**.

---

## 📂 Dataset
The dataset consists of three main files:
- **movies.dat** → Movie IDs, titles, and genres  
- **users.dat** → User demographics (age, gender, occupation, zip-code)  
- **ratings.dat** → User ratings for movies with timestamps  

After preprocessing and merging:
- **Total ratings:** ~1,000,208  
- **Unique users:** ~6,039  
- **Unique movies:** ~3,882  

---

## ⚙️ Workflow
1. **Data Loading & Cleaning**
   - Handle custom separators (`::`) and encoding (`latin-1`)
   - Merge movies, users, and ratings into a single dataframe
   - Create age buckets (`Under 18`, `18–24`, …, `56+`)

2. **Feature Engineering**
    One-hot encode categorical features (Gender, Age, Occupation, Genres)

3. **Model Training**
    ML models: Logistic Regression, SVM, KNN, Decision Tree and Random Forest.

4. **Evaluation**
  - Decision Tree → RMSE ~1.41
  - Random Forest → RMSE ~1.32
  - KNN → RMSE ~1.66
  - Logistic Regression → RMSE ~1.38
  - SVM → RMSE ~1.26 (best so far)
 
5. **Observations**
  - User demographics + genres alone are weak predictors.
  - SVM performed slightly better, but still limited by feature sparsity.
