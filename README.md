# 🎙️ Human Voice Analysis for Age & Gender Estimation
> **Research Project** | Multi-modal Speaker Analysis using MFCC and Machine Learning

[![Status](https://img.shields.io/badge/Status-Completed-success.svg)](#)
[![Tech](https://img.shields.io/badge/Tech-Signal%20Processing%20%7C%20ML-blue.svg)](#)
[![Accuracy](https://img.shields.io/badge/Best%20Age%20Accuracy-97.3%25-orange.svg)](#)

## 📌 Abstract
Age estimation from a speaker’s voice is a critical research area in digital signal processing. This project utilizes **Mel-Frequency Cepstral Coefficients (MFCC)** to extract statistical features from audio clips. The Mel scale divisions mimic the human auditory system's response, providing a "spectrum-of-a-spectrum" depiction of the audio. Post-extraction, various regression and classification models were applied to a custom-labeled dataset to estimate age and identify gender.

## ⚙️ Methodology
The workflow follows a standard digital signal processing and machine learning pipeline:
1.  **Data Acquisition:** Built a labeled dataset by collecting audio samples across diverse age groups (5–75 years) and genders.
2.  **Feature Extraction:** Applied MFCC algorithms to capture nonlinear spectral characteristics.
3.  **Modeling:**
    * **Regression:** Used to compute the specific age of the speaker.
    * **Classification:** Used to identify the gender (Male/Female).



## 📊 Dataset Specifications
* **Source:** Self-prepared dataset compiled from YouTube audio clippings.
* **Age Range:** 5 to 75 years.
* **Genders:** Male and Female.
* **Size:** 494 total samples.
* **Split:** 80% Training | 20% Testing.

## 📈 Results & Performance

### 1. Age Estimation (Regression Models)
The goal was to predict a continuous value representing the speaker's age.

| Model | Accuracy |
| :--- | :--- |
| **Decision Tree Regressor** | **97.3%** |
| Stochastic Gradient Descent (SGD) | 92.6% |
| XGBoost Regressor | 89.0% |
| CatBoost Regressor | 65.7% |

### 2. Gender Detection (Classification Models)
Classification models identified speakers as either male or female.

| Model | Accuracy | Precision | F1-Score |
| :--- | :--- | :--- | :--- |
| **CatBoost Classifier** | **90%** | 90% | 90% |
| XGBoost Classifier | 89% | 88% | 89% |
| SGD Classifier | 88% | 88% | 88% |
| Decision Tree Classifier | 80% | 80% | 80% |

## 🚀 Conclusions
* **Optimal Models:** The **Stochastic Gradient Regressor** and **Decision Tree Regressor** yielded the highest performance for age prediction.
* **Gender Performance:** CatBoost, XGBoost, and SGD provided the most satisfactory results for gender classification.
* **Future Work:** Enhancements will include incorporating linguistic factors such as **accent** and **vocabulary** to improve model robustness and predictive accuracy.

---

### 🛠 Tech Stack
* **Language:** Python
* **Signal Processing:** MFCC, Spectral Analysis
* **ML Libraries:** Scikit-Learn, XGBoost, CatBoost
* **Tools:** Librosa (Audio Analysis)

***
*Note: Developed as part of an academic research focus on Signal Processing and Machine Learning.*
