# SMS Spam Detection Application

This project implements a machine learning pipeline to classify SMS messages as spam or not spam using a Support Vector Machine (SVM) with TF-IDF vectorization. The application includes an interactive web interface built with Gradio for users to input SMS messages and receive predictions.

---

## Table of Contents
1. [Overview](#overview)
2. [Requirements](#requirements)
3. [Dataset](#dataset)
4. [Pipeline Details](#pipeline-details)
5. [How to Run the Application](#how-to-run-the-application)
6. [Testing Examples](#testing-examples)
7. [Usage](#usage)
8. [Future Improvements](#future-improvements)

---

## Overview
The application predicts whether an SMS message is spam or not using a pre-trained machine learning model. It utilizes the following:
- **TF-IDF Vectorization**: Converts text messages into numerical features.
- **Linear Support Vector Classifier (LinearSVC)**: Classifies the messages as spam or not.

The application is packaged with a Gradio interface for easy use and interaction.

---

## Requirements
To run this project, you need the following dependencies:
- `pandas`
- `scikit-learn`
- `gradio`

You can install these dependencies using pip:
```bash
pip install pandas scikit-learn gradio
```


## Dataset
The application uses the `SMSSpamCollection.csv` file as the dataset. The dataset should have the following columns:

- **`text_message`**: The SMS content.
- **`label`**: The classification label (`spam` or `ham`).

Ensure the dataset is located in the `Resources/` directory.

---

## Pipeline Details
The machine learning pipeline includes:

1. **TF-IDF Vectorization**:
   - Converts SMS messages to numerical representations while filtering out common English stop words.
2. **Linear Support Vector Classifier (LinearSVC)**:
   - Trains on the numerical features to predict spam or not.

---

## How to Run the Application
1. Clone this repository and navigate to the project directory.
2. Ensure the dataset is available in the `Resources/SMSSpamCollection.csv` path.
3. Run the Python script:
   ```bash
   python sms_spam_detection.py
4. A Gradio interface will launch in your default web browser.
## Testing Examples
You can test the following SMS messages in the Gradio app:

### Not Spam
- "You are a lucky winner of $5000!"
- "You won 2 free tickets to the Super Bowl."

### Spam
- "You won 2 free tickets to the Super Bowl text us to claim your prize."
- "Thanks for registering. Text 4343 to receive free updates on medicare."

---

## Usage
1. Enter an SMS message in the input box.
2. Click **Submit**.
3. The application will display whether the message is spam or not spam.

---

## Future Improvements
- Enhance the dataset for better performance.
- Add additional evaluation metrics (Precision, Recall, F1-Score) to assess model performance.
- Support multi-language SMS detection.
- Integrate real-time API support for live message classification.

---

## Credits
This application is powered by:

- **Scikit-learn**: For machine learning pipelines.
- **Gradio**: For building an interactive user interface.
