# Insurance-Claims-Classification

## Project Overview

In the insurance industry, accurately predicting the likelihood of claims is essential for effective risk assessment and policy pricing. However, insurance claims datasets often suffer from class imbalance, where non-claims significantly outnumber actual claims. This imbalance can lead to predictive models that are biased towards the majority class, resulting in poor performance in identifying the minority class, which is of greater interest to insurers.

The objective of this project is to develop and evaluate a predictive model that accurately identifies the likelihood of insurance claims, even in the presence of class imbalance. The model is designed to maintain high predictive accuracy across both classes, enabling insurers to effectively assess risk and allocate resources.

## Dataset

Link: https://statso.io/training-models-on-imbalanced-data-case-study/#google_vignette
The dataset used in this project includes various features related to policyholders and their vehicles, along with a target variable, `claim_status`, which indicates whether a claim was made (`1`) or not (`0`). The dataset is preprocessed by encoding categorical variables and dropping irrelevant columns, such as `policy_id`.

## Project Steps

### 1. Data Preprocessing

- **Drop Irrelevant Columns:** The `policy_id` column is dropped from the dataset as it does not contribute to the predictive modeling process.
- **Feature and Target Variables:** The features (`X`) are separated from the target variable (`y`), which represents the claim status.

### 2. Train-Test Split

- The dataset is split into training and testing sets using an 80-20 split ratio, ensuring that the model's performance is evaluated on unseen data.

### 3. Model Training

- **Model Used:** A `RandomForestClassifier` is used for training the model. Random Forest is chosen for its robustness and ability to handle class imbalance effectively.
- **Training Process:** The model is trained on the training set (`X_train`, `y_train`) to learn patterns that predict the likelihood of claims.

### 4. Model Evaluation

- **Accuracy Score:** The model's accuracy is calculated on the test set to measure the overall performance.
- **Classification Report:** A detailed classification report is generated, providing precision, recall, and F1-score for both classes (`claim_status`), as well as overall metrics.
- **Confusion Matrix Visualization:** A heatmap of the confusion matrix is created to visualize the number of correct and incorrect predictions for each class.

### 5. Feature Importance

- The importance of each feature in predicting the `claim_status` is extracted from the trained Random Forest model, allowing for insights into which factors contribute most to the likelihood of a claim.

