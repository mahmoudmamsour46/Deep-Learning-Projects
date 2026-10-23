# 🧠 Deep Learning Projects Portfolio

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00?logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-Deep_Learning-D00000?logo=keras&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine_Learning-F7931E?logo=scikit-learn&logoColor=white)

Welcome to my **Deep Learning Projects** repository! This repository serves as a structured collection of Deep Learning models and experiments built using **Python, TensorFlow, Keras, and Scikit-Learn**, covering both **Regression** and **Classification** tasks.

---

## 📂 Projects Directory

| # | Project Name | Task Type | Dataset | Architecture | Key Performance |
| :-: | :--- | :---: | :--- | :--- | :--- |
| **01** | [**California Housing Price Prediction**](./California%20Housing%20Regression) | 📈 Regression | California Housing (`20,640` samples, `8` features) | 7-Layer Sequential MLP (`ReLU`) | **$R^2 = 79.4\%$** (`MAE = 0.3502`, `RMSE = 0.5269`) |
| **02** | [**Breast Cancer Wisconsin Classification**](./Breast%20Cancer%20Classification) | 🩺 Binary Classification | Breast Cancer Wisconsin (`569` samples, `30` features) | 3-Layer Sequential MLP (`ReLU` + `Sigmoid`) | **Accuracy = $98.25\%$** (`F1 = 0.98`, `Recall (Benign) = 1.00`) |
| **03** | [**TinyML Audio Digits Recognition on STM32**](./TinyML%20Audio%20Digits%20Recognition) | 🎙️ TinyML / Edge Audio | Google Speech Commands (`0–9`) | 3-Layer CNN (`40,812` params) + Linear & PoT PTQ | **Accuracy = $85.03\%$**, **Flash = $45.4\text{ KB}$**, **RAM = $18.8\text{ KB}$**, **Latency = $208\text{ ms}$** |

---

## 🔍 Projects Overview

### 1. [🏠 California Housing Regression](./California%20Housing%20Regression)
- **Objective:** Predict median house values across California districts using a Deep Multi-Layer Perceptron (MLP).
- **Workflow:** Missing/duplicate value checks, `StandardScaler` normalization, Train/Validation/Test split (`72% / 8% / 20%`), 7-layer `Sequential` neural network trained with `SGD` and `MSE` loss over 100 epochs.
- **Results:** Achieved **$R^2$ Score of `0.7939`**, `MAE` of `0.3502`, and `RMSE` of `0.5269`.
- 👉 [**View Project Folder & Documentation**](./California%20Housing%20Regression/README.md)

---

### 2. [🩺 Breast Cancer Classification](./Breast%20Cancer%20Classification)
- **Objective:** Classify breast mass tumors into **Malignant (`0`)** or **Benign (`1`)** from 30 digitized FNA features.
- **Workflow:** Exploratory data analysis, class balance inspection, `StandardScaler` preprocessing, stratified Train/Test split (`80% / 20%`), 3-layer `Sequential` MLP trained with `Adam` and `binary_crossentropy` loss over 100 epochs.
- **Results:** Achieved **`98.25%` Test Accuracy** (`112/114` correct), `1.00` Precision on Malignant cases, and `1.00` Recall on Benign cases.
- 👉 [**View Project Folder & Documentation**](./Breast%20Cancer%20Classification/README.md)

---

### 3. [🎙️ TinyML Audio Digits Recognition on STM32](./TinyML%20Audio%20Digits%20Recognition)
- **Objective:** Practical implementation and edge deployment of the speech digit recognition CNN from the Elsevier (2022) paper onto an **STM32F401 (ARM Cortex-M4)** microcontroller.
- **Quantization Experiments:** Implemented and compared both **True Integer Linear Quantization** and **Power-of-Two (PoT) Bit-Shift Quantization** for zero-multiplication integer arithmetic.
- **Memory & Edge Optimization:** Reduced Flash from **161.4 KB down to 45.4 KB** (3.6x savings) and limited SRAM to **18.8 KB Peak RAM** using Ping-Pong activation buffers (enabling deployment on the 64 KB RAM microcontroller).
- **Physical Hardware Metrics:** Verified live hardware inference with **~208 ms latency**, **85.03% Top-1 Accuracy** (matching the paper's reported ~85%), and direct output to a 7-segment display.
- 👉 [**View Project Folder & Documentation**](./TinyML%20Audio%20Digits%20Recognition/README.md)
- 🔗 [**View Full Dedicated Repository & Embedded C Firmware**](https://github.com/mahmoudmamsour46/TinyML-Audio-Digits-Recognition-STM32)

---

## 🛠️ Tech Stack & Libraries
- **Deep Learning:** TensorFlow, Keras
- **Data Preprocessing & Evaluation:** Scikit-Learn (`StandardScaler`, `train_test_split`, `classification_report`, `confusion_matrix`, Regression metrics)
- **Data Manipulation:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn

---

## 🚀 Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/mahmoudmamsour46/Deep-Learning-Projects.git
   cd Deep-Learning-Projects
   ```

2. **Navigate to any project folder and install requirements:**
   ```bash
   cd "Breast Cancer Classification"
   pip install -r requirements.txt
   jupyter notebook
   ```
