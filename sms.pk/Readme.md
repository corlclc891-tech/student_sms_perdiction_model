# SMS & Intern Feedback Sentiment Analysis using NLP

## 📌 Project Overview

This project implements a **Natural Language Processing (NLP)** and **Machine Learning** pipeline to analyze and classify text-based feedback (e.g., intern reviews, SMS messages) into **Positive** or **Negative** sentiments. Using **TF-IDF Vectorization** and **Logistic Regression**, the system automatically identifies constructive satisfaction levels and flags operational issues needing management attention.

## 🛠️ Key Features

* **Text Preprocessing & Vectorization:** Converts raw textual feedback into numerical feature representations using `TfidfVectorizer` (with English stop-words filtering and lowercase normalization).
* **Machine Learning Classifier:** Trains a **Logistic Regression** model for fast and accurate binary text classification.
* **Model Evaluation:** Evaluates pipeline performance using Accuracy Score and comprehensive Classification Reports (Precision, Recall, F1-Score).
* **Inference Pipeline:** Includes an automated testing loop to predict sentiment labels for new, unseen feedback statements with clear output tags:
  * **Positive Sentiment:** 😊
  * **Negative Sentiment:** ⚠️ *(Flagged for improvement)*

## 📊 Dataset Structure

The project processes textual feedback paired with binary target labels:

| Feature Name | Description | Data Type | Sample |
| :--- | :--- | :--- | :--- |
| `feedback` | Raw textual review or message | String / Text | *"The mentorship was amazing..."* |
| **`sentiment` (Target)** | Classification label ($1 = \text{Positive}, 0 = \text{Negative}$) | Integer | `1` or `0` |

---

## ⚙️ Requirements & Dependencies

To run this script, ensure you have **Python 3.8+** installed along with the following libraries:

```bash
pip install numpy pandas scikit-learn
```

---

## 🚀 How to Run the Script in VS Code

### 1. Open VS Code Terminal
Press `Ctrl + ~` to launch the terminal inside your project directory.

### 2. Run the Python Script
Execute the script using:

```bash
python "sms pd.py.py"
```

---

## 📈 Sample Execution Output

Upon execution, the terminal outputs the evaluation metrics followed by live predictions on unseen feedback:

```text
Model Accuracy: 100.00%

Classification Report:
               precision    recall  f1-score   support

           0       1.00      1.00      1.00         1
           1       1.00      1.00      1.00         1

    accuracy                           1.00         2
   macro avg       1.00      1.00      1.00         2
weighted avg       1.00      1.00      1.00         2


--- NEW FEEDBACK PREDICTIONS & ANALYSIS ---
Feedback: 'Mentors were not available when needed.'
Sentiment: Negative ⚠️ (Needs Improvement)

Feedback: 'The learning opportunities and team guidance were incredible.'
Sentiment: Positive 😊

Feedback: 'Too much pressure and poor communication from management.'
Sentiment: Negative ⚠️ (Needs Improvement)
```

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).