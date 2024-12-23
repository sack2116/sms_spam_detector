# Module 21 SMS Spam Classification with Gradio Interface

This project implements an SMS spam classification model using machine learning and provides a Gradio-based user interface for testing predictions.

## Project Overview

The goal of this project is to classify SMS messages as either "spam" or "ham" (not spam). It involves training a machine learning model using a dataset of labeled SMS messages and deploying the model with an interactive Gradio interface.

## Features

- Preprocessing steps to vectorize SMS text using **TF-IDF Vectorization**.
- Classification using a **Linear Support Vector Classifier (LinearSVC)**.
- Gradio interface for user-friendly input and classification output.

## Data

The dataset `SMSSpamCollection.csv` contains two columns:
- **`label`**: The target column with values "spam" or "ham".
- **`text_message`**: The SMS message content.

### Dataset Summary
- `ham`: 4825 messages
- `spam`: 747 messages
- Total: 5572 messages

## Model Pipeline

1. **TF-IDF Vectorization**: Converts SMS messages into numerical feature representations.
2. **Linear SVC**: A Support Vector Classifier optimized for text classification tasks.

## Gradio Interface

The Gradio app allows users to:
1. Input an SMS message in a text box.
2. Receive real-time classification results ("spam" or "not spam").

## How to Run

### Prerequisites
Ensure the following are installed:
- Python 3.8+
- Required Python libraries (`pandas`, `scikit-learn`, `gradio`)

### Steps to Run

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
2. Run the script either in jupyter or Google Collab
sms_text_classification_solution
Open the Gradio app: Once launched, a local URL will be displayed in the terminal. Open it in your browser to interact with the app.

## Example Inputs and Outputs
Sample Inputs:
1. You are a lucky winner of $5000!
2. You won 2 free tickets to the Super Bowl.
3. Hey, are we still meeting at 2 PM today?
4. Thanks for registering. Text 4343 to receive free updates on Medicare.

## Sample Outputs:
1. Spam: The text message: "You are a lucky winner of $5000!", is spam.
2. Not Spam: The text message: "Hey, are we still meeting at 2 PM today?", is not spam.

## Challenges
Class Imbalance: The dataset has significantly more "ham" messages than "spam." Addressed using class_weight='balanced' in the model.
Gradio Integration: Ensuring smooth integration of the model into a real-time interface for user testing.


## Future Improvements
Implement additional text preprocessing techniques (e.g., stemming, lemmatization).
Explore more advanced models like Random Forests or Neural Networks.
Enhance the Gradio app interface with more customization options.