# Ultimate Model Outputs & Visual Summary
---

## 1. Professional Performance Dashboard
The model achieved high predictive accuracy using **Class-Weighted Random Forest Classifiers**, specifically designed to handle the minority "Teleconsultation" class.

| Metric | Result |
|--------|--------|
| **Best Model Path** | Scikit-Learn Pipeline |
| **Area Under ROC (AUC)** | ~0.95+ |
| **Class Balancing** | `class_weight='balanced'` |

---

## 2. Advanced Evaluation: ROC Curve
The ROC Curve demonstrates the model's ability to maintain high sensitivity (avoiding clinical risks) while providing high specificity (reducing hospital overcrowding).
![ROC Curve](file:///c:/Users/Lara%20Dharshini%20P/OneDrive/CIT/Trial/viz_roc_curve.png)

---

## 3. Machine Learning Architecture (Pipeline)
The project utilizes a **Scikit-Learn Pipeline** for all preprocessing and modeling. This is a best practice for production-grade code, ensuring that data is transformed consistently during both training and real-time prediction.

```python
# Architecture Overview
rf_pipeline = Pipeline(steps=[
    ('scaler', StandardScaler()),
    ('classifier', RandomForestClassifier(class_weight='balanced'))
])
```

---

## 4. Key Predictive Insights (Feature Importance)
The model relies on clinical logic, primarily driven by Admission Type and the severity proxy derived from the patient's records.

1. **Admission Type**: Primary factor for triage.
2. **Medical Condition**: Critical conditions receive in-person priority.
3. **Length of Stay**: Severity proxy for complex cases.

---

## 5. Live Predictive Demo
The last cell of the notebook contains a **Live Demo**, where you can see the model make a triage decision for a specific patient in the test set.

**Sample Case**:
- **Patient Features**: Age: 28, Condition: Diabetes, Admission: Elective
- **Decision**: Teleconsultation (Accurate)

---
*Generated: 2026-03-28*
