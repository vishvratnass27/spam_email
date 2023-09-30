
---

# Spam Email Detection

This repository contains code for a spam email detection project. The goal of this project is to classify emails as either spam or not spam (ham) based on various features of the emails.

## Dataset

The dataset used in this project is named "spam_email_dataset.csv." It contains the following columns:

- `Email`: The email content.
- `Subject`: The subject line of the email.
- `Sender`: The sender's email address.
- `Recipient`: The recipient's email address.
- `Date`: The date the email was sent.
- `Time`: The time the email was sent.
- `Attachments`: The number of attachments in the email.
- `Link Count`: The number of hyperlinks in the email.
- `Word Count`: The total number of words in the email.
- `Uppercase Count`: The number of uppercase letters in the email.
- `Exclamation Count`: The number of exclamation marks in the email.
- `Question Count`: The number of question marks in the email.
- `Dollar Count`: The number of dollar signs in the email.
- `Punctuation Count`: The total number of punctuation marks in the email.
- `HTML Tags Count`: The number of HTML tags in the email.
- `Spam Indicator`: The target variable indicating whether the email is spam (1) or not (0).

## Data Exploration and Preprocessing

- The data was loaded using pandas, and basic information about the dataset was obtained using `E_data.info()` and `E_data.describe()`.
- Missing values were visualized using a heatmap (`sns.heatmap`) and handled appropriately.
- Data visualization was performed using seaborn (`sns.countplot`) to understand the impact of various features on the spam indicator.
- Unnecessary columns such as "Email," "Subject," "Sender," "Recipient," "Date," and "Time" were dropped.
- Categorical variables were one-hot encoded.

## Model Building

Two classification models were trained and evaluated:

1. **Random Forest Classifier**
   - Data was split into training and testing sets using `train_test_split`.
   - A Random Forest Classifier was trained on the training data.
   - Model performance was evaluated using accuracy and a confusion matrix.

2. **Logistic Regression**
   - Data was split into training and testing sets.
   - A Logistic Regression model was trained.
   - Model performance was evaluated using accuracy and a confusion matrix.

## Usage

You can run the code provided in this repository to perform spam email detection. Make sure you have the required libraries installed in your Python environment.

```bash
pip install pandas matplotlib seaborn numpy scikit-learn
```

To run the code, execute the Jupyter Notebook or Python script.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
