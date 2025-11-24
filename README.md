# Fake News Classification (Binary)

This project is a complete pipeline for identifying whether a news article is **Real** or **Fake** using a mix of machine‑learning and deep‑learning models. The entire workflow is contained inside one script: `fakenews.py`. Once executed, the script trains multiple models, evaluates them, and generates a detailed Excel report with all performance metrics.

---

## Project Structure
```
.
├── fakenews.py
├── True.csv
├── Fake.csv
└── Full_Detailed_Report.xlsx    (generated after running the script)
```

- **True.csv** – contains real news articles  
- **Fake.csv** – contains fake news articles  
- **fakenews.py** – full training + evaluation pipeline  
- **Full_Detailed_Report.xlsx** – automatically generated output file

---

## What the Script Does
- Loads and merges both datasets  
- Cleans and preprocesses the text  
- Splits the data into training and testing sets  
- Trains several traditional ML models (Logistic Regression, SVM, Random Forest, XGBoost, etc.)  
- Trains deep-learning models (RNN, GRU, LSTM, Bi-LSTM, CNN, Attention, Transformer)  
- Compares model performance  
- Saves the results into an Excel report for easy review  

Everything runs automatically once you execute the script.

---

## How to Run
1. Keep `True.csv` and `Fake.csv` in the same folder as `fakenews.py`.  
2. Install the required packages:
```
pip install -r requirements.txt
```
3. Run the project:
```
python fakenews.py
```

After execution, the file **Full_Detailed_Report.xlsx** will appear in the same directory.

---

## Requirements
Here are the core libraries used:
```
pandas
numpy
scikit-learn
matplotlib
xgboost
tensorflow
xlsxwriter
openpyxl
nltk
tqdm
```

---

## Output
- A consolidated Excel report with metrics for every model  
- Accuracy, precision, recall, and F1‑score logs in the console  
- Side‑by‑side comparison of ML and DL models  

---

## Notes
- Labels are automatically assigned in the script:  
  - Real news → 1  
  - Fake news → 0  
- If your dataset has a different format or column names, you can modify those sections in `fakenews.py`.

---

## About This Project
I built this project to explore how different models behave on the same text‑classification task. It helped me compare traditional ML methods with modern deep‑learning approaches and understand their strengths and limitations. The goal was to keep the pipeline simple to run, while still covering a wide range of models.

