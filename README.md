# Spam Detection Using Machine Learning

This project classifies messages as **SPAM 🚨** or **HAM ✅** using Python and scikit-learn.

## Features
- Uses **CountVectorizer** for text feature extraction.
- Implements **Naive Bayes classifier** for spam detection.
- Can test single messages or batches of messages.
- Model and vectorizer are saved for future use.

## How to Use
1. Clone the repo:
2. Install required libraries:
pip install -r requirements.txt
3. Run the notebook `spam_detection.ipynb` to see the model in action.
4. Use the saved model to classify new messages:
```python
import joblib
model = joblib.load('spam_classifier_model.pkl')
vectorizer = joblib.load('vectorizer.pkl')
message = ["Your message here"]
vec = vectorizer.transform(message)
prediction = model.predict(vec)
  
