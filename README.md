# 📰 Fake News Detection using Naive Bayes

This project focuses on detecting **fake news** using **Natural Language Processing (NLP)** and **Machine Learning**.  
The main goal is to build a model that can automatically classify news articles as **Fake** or **True**, helping prevent the spread of misinformation.

---

## 📊 Dataset

The dataset used consists of two CSV files:
* **Fake.csv** → contains fake news articles  
* **True.csv** → contains real (true) news articles  

Each file includes:
* `title` – the headline of the article  
* `text` – the full news content  
* `subject` – news category  
* `date` – publication date  

A new column, **label**, was added:
* `0` → Fake news  
* `1` → True news  

---

## ⚙️ Project Workflow

The project follows a clear machine learning pipeline:

1. **Data Loading & Labeling:**  
   Both datasets were loaded using `pandas`, and labels (0, 1) were assigned.

2. **Data Merging:**  
   The two datasets were combined into one, and a new column `content` was created by merging `title` and `text`.

3. **Data Splitting:**  
   The data was divided into **training** and **testing** sets (80% / 20%).

4. **Text Vectorization:**  
   Text data was transformed into numeric form using **TF-IDF Vectorizer**, which highlights important words while ignoring common ones.

5. **Model Training:**  
   A **Multinomial Naive Bayes** model was trained on the TF-IDF vectors.

6. **Model Evaluation:**  
   The model was evaluated using key metrics: Accuracy, Precision, Recall, F1-score, and Confusion Matrix.

---

## 📈 Results & Key Findings

The model showed strong performance in distinguishing fake and real news:

* **Accuracy:** ~94%  
* **Precision:** 0.94  
* **Recall:** 0.93  
* **F1 Score:** 0.93  

These results indicate that the model can reliably detect fake news with minimal false predictions.

### Confusion Matrix

<img width="580" height="453" alt="image" src="https://github.com/user-attachments/assets/9c9d2477-21d1-4518-8242-7e668cec39c0" />


This visualization shows the number of correctly and incorrectly classified articles.  
- The **top-left** and **bottom-right** cells represent correct predictions.  
- The **other cells** represent misclassifications.

---

## 💡 Conclusion

This project demonstrates how **Naive Bayes** and **TF-IDF** can be effectively used to classify news articles.  
It highlights the importance of **text preprocessing** and **balanced evaluation metrics** when working with natural language data.  
