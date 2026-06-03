

# ⚙️ Sprint 3: Optimization & Final Model

## 🎯 Goal

Select the best-performing machine learning model and prepare it for deployment.

---

## 🏆 Final Model Selection

Multiple classification algorithms were trained and evaluated:

* Logistic Regression
* Decision Tree Classifier
* Random Forest Classifier
* Support Vector Machine (SVM)
* Naive Bayes Classifier

### Model Performance

| Model               | Accuracy |
| ------------------- | -------- |
| Logistic Regression | 99.93%   |
| Decision Tree       | 100.00%  |
| Random Forest       | 99.93%   |
| SVM                 | 99.93%   |
| Naive Bayes         | 94.78%   |

The **Decision Tree Classifier** achieved the highest performance with **100% accuracy** on both the training and testing datasets. Therefore, it was selected as the final model for this project.

---

## 🔍 Overfitting Check

| Model               | Training Accuracy | Testing Accuracy |
| ------------------- | ----------------- | ---------------- |
| Logistic Regression | 99.98%            | 99.93%           |
| Decision Tree       | 100.00%           | 100.00%          |
| Random Forest       | 100.00%           | 99.93%           |
| SVM                 | 99.98%            | 99.93%           |
| Naive Bayes         | 94.03%            | 94.78%           |

The results indicate no significant overfitting or underfitting. The Decision Tree model demonstrated perfect generalization on the synthetic disaster dataset.

---

## 💾 Model Serialization

To make the model reusable for deployment, the trained Decision Tree model was serialized using Joblib and saved as a pickle file.

### Saving the Model

```python
import joblib

joblib.dump(best_model, "disaster_prediction_model.pkl")
```

### Loading the Model

```python
import joblib

model = joblib.load("disaster_prediction_model.pkl")
```

---

## 📁 Generated Files

```text
models/
└── disaster_prediction_model.pkl
```

The serialized model file can be loaded directly into web applications such as Streamlit without retraining the model.

---

## ✅ Outcome

* Selected the best-performing model.
* Validated model performance.
* Confirmed no major overfitting issues.
* Saved the trained model using Joblib.
* Prepared the model for deployment in a Streamlit application.
