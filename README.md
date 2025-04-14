
# 🧠 Analysis of Linear and Non-Linear Relationships Between sEMG and Finger Kinematics

> 👩‍🎓 **Author:** Rashmi Katariya  
> 🎓 **Institution:** Department of Electronics and Communication Engineering, DU Pune / DIAT Pune  


---

## 🎯 Objective

To analyze the correlation between **surface EMG signals (sEMG)** and **finger kinematics** using:
- 🔹 **Linear Regression (LR)** for linear patterns
- 🔹 **Random Forest Regressor (RFR)** for non-linear mappings

Goal: Determine which method gives better **R² score** and **lower RMSE** with optimal training/testing time.

---

## 📚 Literature Survey

- *Continuous and Simultaneous Estimation of Finger Kinematics* – Jimson G Ngeo, Tomoya Tamei, Tomohiro Shibata  
- *SVM Based Simultaneous Hand Movement Classification Using sEMG* – Feifei Bian et al.  
- *Kinematic Synergies of Hand Grasps: A Dataset Study* – Jarque-Bou et al.  
- *Extraction of Nonlinear Synergies for Finger Kinematics* – Sanjay Kumar Dwivedi et al.

---

## 🔬 Introduction

- Myoelectric control systems use sEMG to interpret muscle activity
- Accurate estimation of **multi-DOF finger movements** is critical for prosthetics and rehabilitation
- sEMG signals reflect motor intention but are often **non-linear**

---

## 📦 Dataset Description

![image](https://github.com/user-attachments/assets/22cae348-c397-46f9-918e-523737a7af49)


- **sEMG**: 8-channel from extrinsic muscles  
- **Kinematics**: 3D data from 23 markers → 69-dimensional space  
- **Participants**: 10 subjects (9M, 1F, ages 26–31)  
- **Tasks**:
  - IFFE: Individual finger flexion-extension
  - AFFE: All fingers flexion-extension
  - RFFE: Random combinations

Each subject has:
- `35 trials` → `4000×8` sEMG and `4000×69` kinematic data per trial  
- Total: `140,000 samples per subject`

---

## 🧠 Methodology

- Preprocess sEMG and kinematics data
- Train LR and RFR models **per subject**
- Evaluate using:
  - 🔹 **Root Mean Squared Error (RMSE)**
  - 🔹 **R² Score**

---

## 📊 Algorithms Used

- Linear Regressor  
- Decision Tree Regressor  
- K-Nearest Neighbors  
- ✅ **Random Forest Regressor** (Best performer)

---

## 🧾 Results Summary

| Metric            | LR Model     | RFR Model    |
|-------------------|--------------|--------------|
| RMSE Range        | 5.58 – 9.55  | 0.50 – 1.19  |
| R² Score Range    | 0.17 – 0.47  | 0.98 – 0.99  |
| Mean RMSE         | 7.842        | 0.737        |
| Mean R² Score     | 0.313        | 0.988        |
| Testing Time      | 96 µs        | 94 µs        |

---

### 📈 Visual Results

#### Subject-wise R² Score and RMSE Comparison  
![image](https://github.com/user-attachments/assets/509c121b-7e90-4f90-8e99-036aa02af9cf)



## ✅ Conclusion

- Strong correlation exists between **muscle activations and finger kinematics**
- **Random Forest Regressor** effectively models non-linear dependencies
- Ideal for **myoelectric control** in multi-DOF prosthetics

---

## 📄 References

1. [Ngeo et al. – EMG-to-Muscle Activation Modeling](https://doi.org/10.3389/fnbot.2014.00003)  
2. [Feifei Bian et al. – SVM for Hand Movement Classification](https://ieeexplore.ieee.org/document/7366340)  
3. [Jarque-Bou et al. – Kinematic Synergies Study](https://www.mdpi.com/1424-8220/19/2/452)  
4. [Dwivedi et al. – Nonlinear Synergies & Finger Kinematics](https://ieeexplore.ieee.org/document/6860492)

---

## 🙋‍♀️ Author

**Rashmi Katariya**  
📍 M.Tech – Electronics & Communication  
📬 *Open to collaboration and research discussions*

---

> This repository presents the research phase of an M.Tech dissertation project conducted under DIAT Pune.
