#  SMS Spam Classifier

A complete end-to-end Machine Learning project that classifies SMS/Email messages as **Spam** or **Not Spam** using Natural Language Processing (NLP) techniques and an interactive Streamlit web application.

---

##  Project Overview

This project focuses on detecting spam messages by analyzing text data. It includes the full pipeline from **data preprocessing and feature extraction** to **model training and deployment**.

The final model is integrated into a **Streamlit web app** where users can input a message and instantly get predictions.

---

##  Dataset Information

* **Dataset Name:** SMS Spam Collection Dataset
* **Format:** CSV file
* **Total Records:** ~5,500 messages
* **Columns:**

  * `label` → spam or ham (not spam)
  * `message` → actual text message

###  Data Characteristics

* Text data with informal language, abbreviations, and noise
* Imbalanced distribution (more ham than spam)
* Requires preprocessing for meaningful feature extraction

---

##  Project Workflow

### 1. Data Cleaning

* Removed null values and duplicates
* Renamed columns for better readability

### 2. Exploratory Data Analysis (EDA)

* Checked class distribution (spam vs ham)
* Analyzed message lengths
* Visualized most frequent words

### 3. Text Preprocessing

Performed using NLTK:

* Lowercasing
* Tokenization
* Removal of stopwords and punctuation
* Stemming using Porter Stemmer

---

### 4. Feature Engineering

* Converted text into numerical form using **TF-IDF Vectorization**
* Created a feature matrix for model training

---

### 5. Model Building

* Trained classification models using Scikit-learn
* Selected best-performing model based on accuracy and precision

---

### 6. Model Deployment

* Saved trained model (`model.pkl`)
* Saved vectorizer (`vectorizer.pkl`)
* Built UI using Streamlit

---

##  How It Works

1. User enters a message in the web app
2. Message is preprocessed using NLP techniques
3. TF-IDF converts text into numerical vector
4. Model predicts:

   * **Spam**
   * **Not Spam**

---

##  Tech Stack

* **Programming Language:** Python
* **Libraries:**

  * Scikit-learn
  * NLTK
  * Pandas
  * NumPy
  * Matplotlib / Seaborn
* **Deployment:** Streamlit

---

##  Project Structure

```id="s9df2k"
spam-classifier/
│
├── app.py
├── requirements.txt
├── README.md
│
├── models/
│   ├── model.pkl
│   └── vectorizer.pkl
│
├── data/
│   └── spam.csv
│
├── notebooks/
│   └── sms_sc.ipynb
│
└── screenshots/
    └── app_demo.png
```

---

##  Installation & Setup

1. Clone the repository:

```id="k29dke"
git clone https://github.com/Darshnajain11/SMS-Spam-Classifier.git
cd SMS-Spam-Classifier
```

2. Install dependencies:

```id="p9xw2n"
pip install -r requirements.txt
```

3. Run the application:

```id="z92ksl"
streamlit run app.py
```

---


##  Results

* Achieved high accuracy in spam detection
* Efficient handling of text data using TF-IDF
* Fast real-time predictions via web app

---

##  Future Enhancements

* Deploy on Streamlit Cloud / Azure
* Use advanced models like LSTM or BERT
* Add support for multiple languages
* Improve performance with hyperparameter tuning

---


## ⭐ Conclusion

This project demonstrates how NLP and Machine Learning can be combined to solve real-world problems like spam detection, transforming raw text into meaningful insights and predictions.
