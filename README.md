# 🧮 Student Math Score Prediction using Deep Learning

## 📌 Project Summary
This project predicts a student's math score using demographic and performance data. The model uses a deep neural network built with TensorFlow/Keras and applies proper data preprocessing, feature engineering, and regularization techniques for strong performance and generalization.

---

## 📂 Dataset
- **Source**: [Kaggle – Student Performance Dataset](https://www.kaggle.com/spscientist/students-performance-in-exams)
- **Size**: ~1,000 records with 5 categorical and 3 numerical features
- **Target Variable**: `math score`

---

## 🔨 Tools & Technologies
- Python
- TensorFlow / Keras
- Pandas, NumPy
- Scikit-learn (StandardScaler, OneHotEncoder, ColumnTransformer, metrics)
- Matplotlib & Seaborn for visualization

---

## 🔍 Feature Engineering
- Created a new column:  
  `writing_reading_score = writing score / reading score`  
  This captures proportional understanding across language-based test sections.

---

## 🧠 Model Architecture
```text
Input → Dense(82) → BatchNormalization → ReLU → Dropout(0.3)
      → Dense(35) → BatchNormalization → ReLU → Dropout(0.2)
      → Output (1 neuron for regression)
