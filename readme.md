# Email/SMS Spam Classifier Project (Binary Classification Problem)

# Overview

This project is a web-based application designed to classify Email/SMS messages as **SPAM** or **NOT SPAM** using machine learning models. The project is deployed on Render and utilizes a voting ensemble model combining Multinomial Naive Bayes and ExtraTreesClassifier, achieving 100% precision and 98.55% accuracy.

# Business Use Case

This spam classifier aims to enhance email and messaging systems by accurately filtering out spam messages, thereby increasing productivity and security for users. Unlike other classifiers, this project leverages an ensemble approach combining Multinomial Naive Bayes and ExtraTreesClassifier, achieving 100% precision in spam detection. This high level of accuracy ensures minimal false positives and negatives, making it a reliable tool for industry applications.

# Features

- Text preprocessing with spaCy
- TF-IDF vectorization of input text
- Multiple machine learning models for spam classification
- Ensemble model for improved accuracy
- JSON-based API for predictions
- User-friendly web interface

# Prerequisites

- Python 3.7 or higher
- Flask
- spaCy and its English model (en_core_web_md)
- scikit-learn
- pickle

# Installation

### Clone the repository:

```
git clone https://github.com/yourusername/spam-classifier.git
cd spam-classifier
```

### Install required packages:

```python
pip install -r requirements.txt
```

### Download and install spaCy English model:

```python
python -m spacy download en_core_web_md
```

### Usage:

1. Start the Flask app:

```python
python app.py
```

2. Access the application at http://0.0.0.0:8000.

# Project Details

### Project Structure:

1. `Dataset`:

   - spam.csv: The dataset used for training and testing the models.
2. `static`:

   - Background image and style.css: Static files for the web application's appearance.
3. `templates`:

   - `index.html`: The main HTML file for the web application's interface.
4. `application.py`: The main Flask application script.
5. `dockerfile`: Docker configuration file for containerizing the application.
6. `requirements.txt`: List of dependencies required for the project.
7. `email_spam_detector.ipynb`: Jupyter notebook for model training and experimentation.

### Functions and Their Purpose:

- `transform_text(text)`: Preprocesses the input text by converting to lowercase, tokenizing, removing stopwords and punctuation, and lemmatizing the tokens.
- `Flask route home()`: Handles GET and POST requests for the home page, processes input SMS, vectorizes it, and returns the prediction.

### Model Training and Experimentation:

The model was first trained using Naive Bayes and then Multinomial Naive Bayes, which achieved 100% precision. Further experimentation involved various models, including:

- **Logistic Regression**
- **SVC**
- **Decision Tree Classifier**
- **K-Nearest Neighbors**
- **Random Forest Classifier**
- **AdaBoost Classifier**
- **Bagging Classifier**
- **ExtraTreesClassifier**
- **Gradient Boosting Classifier**
- **XGBoost Classifier**

Finally, a `Voting Ensemble` was created with `Multinomial Naive Bayes` and `ExtraTreesClassifier`, which improved the model accuracy further while maintaining 100% precision. This extensive experimentation ensures the robustness and reliability of the spam classifier.

## How to Use the Application:

- Open the application in your browser.
- Enter an SMS message in the input field.
- Click the "Predict" button.
- View the prediction result indicating whether the message is **SPAM** or **NOT SPAM**.

# Deployment

The application is deployed on a Cloud Platform `Render`.

You can access the application using the given Deployment Link: Email Spam Classifier

# Contributing

- Fork the repository.
- Create a new branch (git checkout -b feature-branch).
- Commit your changes (git commit -am 'Add new feature').
- Push to the branch (git push origin feature-branch).
- Create a new Pull Request.

# License

This project is licensed under the `MIT` License.
