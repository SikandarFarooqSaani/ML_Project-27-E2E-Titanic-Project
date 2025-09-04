# 🚢 Titanic Survival Prediction  

![Titanic Logo](https://img.icons8.com/emoji/96/ship.png)  

---

## 📌 Project Overview  
This is an **End-to-End Machine Learning project** predicting whether a passenger would survive the **Titanic disaster** 🌊.  
The project includes **data preprocessing, model building, hyperparameter tuning, bagging, voting ensembles**, and finally **deployment on Streamlit**.  

👉 **Live Demo:** [Streamlit App](https://lyzzxl47b7r4hvlhu79x27.streamlit.app/)  
📂 **GitHub Repo:** [Titanic Survival Prediction](https://github.com/SikandarFarooqSaani/Project-TitanicSurvivalPrediction)  

---

## 📂 Dataset & Features  
The dataset is from the famous **Kaggle Titanic Competition**.  

We used **5 key features** for survival prediction:  
- Passenger Class 🎟️  
- Sex 👨‍🦰👩‍🦰  
- Age 🎂  
- Fare 💰  
- Port of Embarkation ⚓  

---

## ⚙️ Tech Stack & Libraries  
- **Python** 🐍  
- **Pandas, NumPy** → Data handling  
- **Scikit-learn** → ML models, Bagging, RandomizedSearchCV  
- **Matplotlib, Seaborn** → Visualization  
- **Joblib** → Saving models (`.pkl`)  
- **Streamlit** → Deployment  

---

## 🛠️ Data Preprocessing  
- Dropped unnecessary columns 🗑️  
- Filled missing values (NA)  
- Removed duplicates  
- Converted datatypes (this was a tricky part 😅)  
- Applied **Label Encoding** to categorical columns  
- Saved the **cleaned dataset** for later use  

---

## 🚀 Models & Experiments  

### 🔹 Base Models  
- Logistic Regression → **0.76**  
- Decision Tree → **0.69**  
- KNN → **0.70**  

📊 Confusion Matrices (attached in repo):  
- Many misclassifications, especially False Negatives  
- KNN performed worst (likely due to **curse of dimensionality**)  

<img width="649" height="547" alt="27-1" src="https://github.com/user-attachments/assets/f2de4e36-8bfa-4a59-b562-468302ab2879" />

<img width="649" height="547" alt="27-2" src="https://github.com/user-attachments/assets/608610bc-1269-45e4-9271-c2b4e048c15c" />
<img width="649" height="547" alt="27-3" src="https://github.com/user-attachments/assets/3fae3ece-c3fc-4ca8-a845-1765eed34f1f" />




---

### 🔹 Hyperparameter Tuning (RandomizedSearchCV)  
- Logistic Regression → **0.78** (best score)  
- Decision Tree → **0.78**  
- KNN → **0.74**  

Best parameters were displayed in the notebook.  
<img width="649" height="547" alt="27-4" src="https://github.com/user-attachments/assets/a9cb0003-5f89-47c9-bfc3-bc2dca493afc" />

---

### 🔹 Voting Classifier  
- Combined tuned Logistic, Decision Tree & KNN  
- Cross-Val Score → **0.78**  
- Accuracy → **0.77**  
- Confusion Matrix attached  
<img width="649" height="547" alt="27-5" src="https://github.com/user-attachments/assets/4fbdae26-41db-4d25-a011-d680bed93b3c" />

---

### 🔹 Bagging  
- Bagging with Decision Tree → **0.79** ✅ (best balance of precision & recall)  
- Bagging with Logistic Regression → **0.76**  
- Bagging with KNN → **0.74**  

Confusion matrices for each are attached.  
<img width="649" height="547" alt="27-6" src="https://github.com/user-attachments/assets/d2acba10-8354-4f84-ac23-85447b278f61" />

<img width="649" height="547" alt="27-7" src="https://github.com/user-attachments/assets/c63bfb78-16e5-43ea-b9da-9df0e8d49f06" />

<img width="649" height="547" alt="27-8" src="https://github.com/user-attachments/assets/4150b89e-6482-4796-9efc-f059543ede2d" />



---

### 🔹 Advanced Models  
- Random Forest → **0.73** (default), improved to **0.75** after tuning  
  - FN = 33, FP = 36  
- AdaBoost → **0.8053** (best so far 🎉)  
  - FN = 15, FP = 36  
  - After tuning → **0.80 accuracy**  

---

## 📊 Results  

| Model                          | Accuracy | Notes |
|--------------------------------|----------|-------|
| Logistic Regression            | 0.76     | Baseline |
| Decision Tree                  | 0.69     | Overfit tendencies |
| KNN                            | 0.70     | Struggled with high dimensions |
| Voting Classifier (tuned)      | 0.77     | Balanced ensemble |
| Bagging (Decision Tree)        | **0.79** ✅ | Best recall/precision |
| Random Forest                  | 0.73–0.75 | Improved after tuning |
| AdaBoost                       | **0.80–0.8053** 🏆 | Best overall |

---

## 💡 Key Takeaways  
- Preprocessing was **the hardest part** of this dataset 💀  
- Logistic Regression held up surprisingly well ⚡  
- KNN struggled due to **curse of dimensionality**  
- Bagging with Decision Tree was **the most stable** option  
- **AdaBoost performed best overall** with **0.80+ accuracy** 🎯  
- Learned a lot about **ensembles, hyperparameter tuning, and model saving**  

---

## 🎯 Conclusion  
This project gave me **hands-on intuition of how ensembles improve predictions**.  
It’s not the perfect Kaggle solution, but as a learner, I feel I’ve **leveled up** 🚀.  

I will continue experimenting by adding more models and improving feature engineering. A new notebook with **Random Forest & AdaBoost experiments** is already included in the repo.  

---

✨ *Survival isn’t luck — it’s feature engineering!* 😅  
