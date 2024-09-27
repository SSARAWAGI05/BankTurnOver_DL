# Customer Churn Prediction

This project implements a machine learning model using TensorFlow to predict customer churn for a bank dataset. The dataset contains various customer attributes, and the model aims to classify whether a customer will exit or remain with the bank.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Modeling](#modeling)
- [Results](#results)
- [License](#license)

## Introduction

Customer churn prediction is critical for businesses to retain customers and improve their services. This project utilizes different techniques, including oversampling, SMOTE, and a neural network model to handle imbalanced data and accurately predict customer behavior.

## Dataset

The dataset used for this project is `Churn_Modelling.csv`, which contains the following columns:

- **RowNumber**: Index of the row.
- **CustomerId**: Unique identifier for each customer.
- **Surname**: Customer's surname.
- **CreditScore**: Credit score of the customer.
- **Geography**: Country of the customer.
- **Gender**: Gender of the customer.
- **Age**: Age of the customer.
- **Tenure**: Number of years the customer has been with the bank.
- **Balance**: Account balance of the customer.
- **NumOfProducts**: Number of products held by the customer.
- **HasCrCard**: Whether the customer has a credit card.
- **IsActiveMember**: Whether the customer is an active member.
- **EstimatedSalary**: Estimated salary of the customer.
- **Exited**: Whether the customer has exited the bank (1 for yes, 0 for no).

## Installation

To run this project, you need to have Python installed along with the following libraries:

- TensorFlow
- Pandas
- NumPy
- Scikit-learn
- imbalanced-learn
- Matplotlib
- Seaborn

You can install the required libraries using pip:

```bash
pip install tensorflow pandas numpy scikit-learn imbalanced-learn matplotlib seaborn
```

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/SSARAWAGI05/BankTurnOver_DL.git
   cd BankTurnOver_DL
   ```

2. Place the `Churn_Modelling.csv` file in the project directory.

## Modeling

The following steps were performed in modeling:

1. **Data Preprocessing**:
   - Drop unnecessary columns (`RowNumber`, `CustomerId`, `Surname`, and `Exited`).
   - Scale numerical features using MinMaxScaler.
   - Convert categorical variables into dummy/indicator variables.

2. **Handling Imbalanced Data**:
   - Two techniques were used:
     - **Oversampling**: The minority class (exited customers) was oversampled to match the majority class.
     - **SMOTE**: Synthetic samples were created for the minority class.

3. **Train-Test Split**: Data was split into training and testing sets.

4. **Model Training**: A neural network model was built using TensorFlow/Keras with the following architecture:
   - Input layer: 12 features
   - 4 hidden layers with ReLU activation
   - Output layer with a sigmoid activation function

5. **Model Evaluation**: The model was evaluated using accuracy and a classification report, along with a confusion matrix visualized using Seaborn.

## Results

- **Model Accuracy**: The model achieved an accuracy of approximately 77% on the test set.
- **Classification Report**: Includes precision, recall, and F1-score for both classes.
- **Confusion Matrix**: A visual representation of the model's predictions against the actual labels.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```
