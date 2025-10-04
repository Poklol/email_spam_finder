# Email Spam Classification Using Python & Machine Learning

A comprehensive machine learning project that uses Natural Language Processing (NLP) and Logistic Regression to classify email messages as spam or ham (legitimate emails). The project includes both a Jupyter notebook for training and a Flask web application for real-time email classification.

## 🚀 Features

- **Machine Learning Model**: Logistic Regression trained on TF-IDF features
- **High Accuracy**: Achieves 96.5% accuracy on test data
- **Web Interface**: User-friendly Flask web application for real-time classification
- **Comprehensive Analysis**: Detailed Jupyter notebook with data exploration and model training
- **Production Ready**: Includes model serialization and deployment setup

## 📋 Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [How It Works](#how-it-works)
- [Model Performance](#model-performance)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)

## 🔧 Installation

### Prerequisites

- Python 3.8 or higher
- pip package manager
- Git

### Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Chando0185/Email_Spam_Classification.git
   cd Email_Spam_Classification
   ```

2. **Create a virtual environment (recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the web application:**
   ```bash
   python app.py
   ```
   The application will be available at `http://localhost:5000`

## 🎯 Usage

### Web Application

1. Open your browser and navigate to `http://localhost:5000`
2. Enter an email message in the text area
3. Click "Classify" to get the prediction
4. The model will return either "Spam" or "Ham" classification

### Jupyter Notebook

1. Open `Email Spam Classification Using Python.ipynb` in Jupyter
2. Run all cells to see the complete training process
3. The notebook includes:
   - Data exploration and preprocessing
   - Feature extraction using TF-IDF
   - Model training and evaluation
   - Prediction examples

### Example Usage

```python
# Using the trained model for prediction
from app import predict_mail

# Example spam email
spam_email = "Congratulations! You've won $1,000,000! Click here to claim your prize!"
result = predict_mail(spam_email)
print(result)  # Output: [0] (Spam)

# Example ham email
ham_email = "Hi John, are we still meeting at 3 PM tomorrow?"
result = predict_mail(ham_email)
print(result)  # Output: [1] (Ham)
```

## 📁 Project Structure

```
Email_Spam_Classification/
│
├── Email Spam Classification Using Python.ipynb  # Main Jupyter notebook
├── app.py                                        # Flask web application
├── requirements.txt                             # Python dependencies
├── mail_data.csv                                # Dataset
├── feature_extraction.pkl                       # Trained TF-IDF vectorizer
├── logistic_regression.pkl                      # Trained model
├── templates/
│   └── index.html                               # Web interface
├── venv/                                        # Virtual environment
└── README.md                                    # Project documentation
```

## 🔍 How It Works

### Data Preprocessing

1. **Text Cleaning**: Email messages are cleaned and normalized
2. **Label Encoding**: Spam/Ham labels are converted to binary (0/1)
3. **Feature Extraction**: TF-IDF (Term Frequency-Inverse Document Frequency) vectorization transforms text into numerical features

### Model Architecture

- **Algorithm**: Logistic Regression
- **Features**: TF-IDF vectorized text features
- **Training**: Uses 80% of data for training, 20% for testing
- **Evaluation**: Accuracy score and model performance metrics

### Classification Process

1. **Input**: Raw email text
2. **Feature Extraction**: Transform text using trained TF-IDF vectorizer
3. **Prediction**: Apply logistic regression model
4. **Output**: Binary classification (0 = Spam, 1 = Ham)

## 📊 Model Performance

- **Training Accuracy**: 96.50%
- **Test Accuracy**: 96.59%
- **Dataset Size**: 5,572 emails
- **Spam/Ham Ratio**: Approximately 1:6 (Spam:Ham)

## 🛠 Technologies Used

- **Programming Language**: Python 3.8+
- **Machine Learning**:
  - Scikit-learn (Logistic Regression, TF-IDF Vectorizer)
  - Pandas (Data manipulation)
  - NumPy (Numerical computing)
- **Web Framework**: Flask
- **Data Format**: CSV
- **Model Serialization**: Pickle
- **Development**: Jupyter Notebook

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

### Areas for Improvement

- [ ] Add more sophisticated NLP preprocessing
- [ ] Implement additional ML algorithms for comparison
- [ ] Add cross-validation
- [ ] Create API endpoints for integration
- [ ] Add unit tests
- [ ] Implement model versioning

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 📞 Contact

- **Author**: Charukesh.B
- **GitHub**: https://github.com/Poklol
- **Email**: charukesh.baskaran@gmail.com

---

⭐ If you found this project helpful, please give it a star!

**Note**: This project uses a sample dataset for demonstration purposes. In production, ensure you comply with data privacy regulations and obtain proper consent for email data usage.
