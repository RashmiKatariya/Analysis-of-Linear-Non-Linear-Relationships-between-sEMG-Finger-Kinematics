
# ✋ Extraction of Nonlinear Synergies for Proportional and Simultaneous Estimation of Finger Kinematics

> 📌 *M.Tech Thesis – Phase I Submission*  
> 👩‍🎓 **Author:** Rashmi Katariya  
> 🎓 **Institution:** Department of Electronics and Communication Engineering, DU Pune  
> 👨‍🏫 **Supervisor:** Dr. Rishi Raj Sharma

---

## 📌 Problem Statement

Understanding and estimating finger movements using **surface Electromyography (sEMG)** is crucial for the development of intelligent prosthetics, rehabilitation devices, and human-robot interfaces. The complexity arises from the **nonlinear and simultaneous nature** of muscle activations during finger movements.

This project aims to achieve **proportional and simultaneous estimation of finger kinematics** using advanced regression models trained on multivariate sEMG signals.

---

## 🎯 Objective

To build a machine learning framework that:
- Extracts meaningful synergies from nonlinear EMG signals
- Predicts 3D hand kinematics from 8-channel sEMG input
- Enables precise and simultaneous estimation of multi-finger movements

---

## 📚 Literature Review

- 🧠 *Nonlinear Synergy Extraction* – [Dwivedi, Ngeo, Shibata (IEEE)](https://ieeexplore.ieee.org/document/6860492)  
- ✋ *Kinematic Synergies in Hand Grasps* – [Jarque-Bou et al. (MDPI)](https://www.mdpi.com/1424-8220/19/2/452)  
- ⚙️ *Linear and Nonlinear Regression for EMG Control* – [J. Hahne et al. (IEEE TNSRE)](https://ieeexplore.ieee.org/document/6548357)  
- 🤖 *EMG-based Classification for Robotic Control* – [Alimohammadi et al.](https://www.sciencedirect.com/science/article/pii/S2405896319304116)

---

## 🖼️ Introduction

![Myoelectric Hand](https://upload.wikimedia.org/wikipedia/commons/0/08/Myoelectric_Hand.jpg)

The system uses surface EMG signals obtained from 8 extrinsic hand muscles. This bio-signal data, in combination with **23 motion-captured markers** (total 69 dimensions), allows modeling finger movement patterns in 3D space.

---

## 📦 Dataset Overview

- **Subjects**: 10 participants (9 Male, 1 Female, aged 26–31)
- **Signals**: 8-channel sEMG + 69-dimensional 3D kinematics
- **Tasks**:
  - IFFE – Individual Finger Flexion-Extension
  - AFFE – All Finger Flexion-Extension
  - RFFE – Random Finger Flexion-Extension
- **Structure**: `5x7` matrix per subject, each cell = `4000x8` (EMG) and `4000x69` (kinematics)

📊 **Sample Matrix**:
```
[ Task1, Task2, ..., Task7 ]
[ Trial1, Trial2, ..., Trial5 ]
Each Cell → EMG: 4000x8, Kinematics: 4000x69
```

---

## 🔁 Model Training Pipeline

- Each subject’s data is trained **independently**
- **Total Data Per Subject**: 140,000 samples
- **Features**: 8-channel EMG  
- **Target**: 69-dimensional finger kinematics

---

## 🤖 Machine Learning Models

We applied and compared various **regression algorithms** for performance:

| Model                     | Type        |
|--------------------------|-------------|
| Linear Regressor         | Linear      |
| Decision Tree Regressor  | Nonlinear   |
| Random Forest Regressor  | Ensemble    |
| K-Nearest Neighbors (KNN)| Lazy Learning |

---

## 🔍 KNN Regressor Pipeline

1. Preprocessing of EMG signals  
2. Dimensionality check  
3. Train-test split  
4. Hyperparameter tuning (value of `k`)  
5. Performance evaluation using metrics like RMSE and R² score

---

## 🧪 Future Work

- Add deep learning-based approaches (LSTM/Conv1D)  
- Implement real-time estimation and visualization  
- Compare across larger, multi-subject datasets  
- Expand to full-hand gesture estimation and control  

---

## 🙋‍♀️ Author

**Rashmi Katariya**  
🎓 M.Tech (Electronics & Communication), DU Pune  
📧 *Reach out for collaboration or research discussion!*

---

> _This work is part of a thesis submitted for the partial fulfillment of the requirements of the M.Tech program._
