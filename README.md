# 🧠 Predicting Ride Cancellations – YourCabs.com

## 🗂 Project Overview

This project aims to predict the **likelihood of a ride cancellation** based on behavioral and platform features provided by YourCabs.com.

We tested multiple classification models to determine which would most accurately forecast cancellations, and identified **Support Vector Machines with RBF kernels** as the top performer.

---

## 📊 Dataset Description

- Source: YourCabs.com (fictitious)
- Key Features:
  - `travel_type_id`: Type of ride (e.g. airport, city)
  - `online_booking`, `mobile_site_booking`: Platform used for booking
  - `Car_Cancellation`: Target variable (0 = Not Cancelled, 1 = Cancelled)

---

## 🔍 Techniques Used

### 📌 A. Naive Bayes
- Trained using `klaR` package
- Model 1: Used only `online_booking`, `mobile_site_booking`
- Model 2: Added `travel_type_id` ➝ Improved accuracy to **92%**

### 📌 B. Decision Trees (C5.0)
- Visualizes which features most impact cancellations
- Boosted model used 10 trials
- Achieved high performance

### 📌 C. ANN (Artificial Neural Networks)
- Used `neuralnet` with dummy encoding
- Model: 3 hidden neurons
- Achieved **92.6% accuracy**

### 📌 D. Support Vector Machine (SVM)
- Model 1: Linear Kernel → Moderate accuracy
- Model 2: RBF Kernel → Best accuracy (92%)
- Tuned cost parameters to balance flexibility vs overfitting

---

## 📈 Performance Summary

| Model         | Accuracy (%) |
|---------------|--------------|
| Naive Bayes (with travel_type_id) | 92.0 |
| Decision Tree (Boosted)           | ~92.0 |
| ANN (3 Hidden Neurons)            | 92.6 |
| SVM (RBF Kernel)                  | **Best** |

> All models had statistically significant predictive power (p < 2e-16)




