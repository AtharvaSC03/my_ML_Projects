
```markdown
# 🧮 Student Exam Performance Prediction

## 📌 Project Overview
This project builds an **end-to-end Machine Learning Pipeline** to predict **Math Scores** of students based on demographic and academic features such as gender, ethnicity, parental education, lunch type, test preparation course, and their reading/writing scores.

The pipeline automates **data preprocessing, model training, evaluation, and deployment**. A web interface (Flask + HTML) is provided for real-time predictions.

---

## 📂 Dataset
- File: `stud.csv`  
- Features include:
  - **Gender**
  - **Race/Ethnicity**
  - **Parental Level of Education**
  - **Lunch Type**
  - **Test Preparation Course**
  - **Reading Score**
  - **Writing Score**
- **Target Variable**: Math Score

---

## ⚙️ ML Pipeline
The project uses multiple regression models with parameters managed in a **YAML configuration file** (`params.yml`), making it easy to update and tune hyperparameters without touching the code.

### Models Used:
- Random Forest Regressor  
- Decision Tree Regressor  
- Gradient Boosting Regressor  
- Linear Regression  
- XGBoost Regressor  
- CatBoost Regressor  
- AdaBoost Regressor  

### Best Model:
- **R² Score: 0.8795** 🎯  
- The pipeline automatically selects the best-performing model and saves it as `artifacts/model.pkl`.

---

## 🚀 Project Structure
```

my\_ML\_Projects/
│── app.py                  # Flask app entry
│── application.py          # Alternative entry point
│── requirements.txt        # Dependencies
│── setup.py                # Packaging file
│── params.yml              # Model hyperparameters
│── artifacts/              # Saved model artifacts
│── notebook/               # Jupyter notebooks for EDA
│── src/                    # Core ML pipeline code
│   ├── components/         # Data ingestion, transformation, training
│   ├── utils.py            # Helper functions
│   ├── logger.py           # Logging setup
│   └── exception.py        # Custom error handling
│── templates/              # HTML templates for Flask UI
│── stud.csv                # Dataset
└── README.md               # Project documentation

````

---

## 💻 How to Run

### 1️⃣ Clone the repository
```bash
git clone https://github.com/AtharvaSC03/my_ML_Projects.git
cd my_ML_Projects
````

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Train the pipeline

```bash
python src/components/model_trainer.py
```

### 4️⃣ Run the web app

```bash
python app.py
```

Then open **[http://127.0.0.1:5000/](http://127.0.0.1:5000/)** in your browser.

---

## 🌐 Web Application

* Input student details through a **user-friendly HTML form**.
* Get real-time prediction of **Math Score**.

---

## 📊 Results

* Achieved **R² Score = 0.8795** on test data.
* Best model auto-selected and stored as a pickle file (`artifacts/model.pkl`).

![Model Score](df877c2a-e245-453e-a0b6-5b130fedae2b.png)

---

## 🛠️ Tech Stack

* **Python** (Scikit-learn, XGBoost, CatBoost, Pandas, NumPy)
* **Flask** (for deployment)
* **HTML/CSS, Bootstrap** (for UI)
* **PyYAML** (config management)
* **Logging + Exception Handling**

---

## 📌 Future Improvements

* Hyperparameter tuning with Optuna/MLflow.
* Model explainability (SHAP, LIME).
* Deploy on AWS/GCP/Heroku.

```

---
##  Results
```
