# Linear Regression - Project Exercise

## Project Overview

Congratulations! You just got some contract work with an Ecommerce company based in New York City that sells clothing online and also provides in-store style and clothing advice sessions. Customers can visit the store, have meetings with a personal stylist, and then order clothes through a mobile app or website.

The company is trying to decide whether to focus their efforts on improving the mobile app experience or the website. They've hired you to analyze the customer data to help them make this decision.

## Table of Contents

1. [Project Description](#project-description)
2. [Data Description](#data-description)
3. [Setup and Installation](#setup-and-installation)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
5. [Modeling](#modeling)
6. [Model Evaluation](#model-evaluation)
7. [Conclusion](#conclusion)
8. [Next Steps](#next-steps)

## Project Description

This project involves analyzing customer data using Linear Regression to determine whether the company should focus on their mobile app or website. The analysis includes exploring the relationships between different features and the yearly amount spent by customers.

## Data Description

The dataset contains customer information such as:

- **Email**: Customer's email address
- **Address**: Customer's address
- **Avatar**: Customer's avatar color
- **Avg. Session Length**: Average session length of in-store style advice sessions
- **Time on App**: Average time spent on the mobile app in minutes
- **Time on Website**: Average time spent on the website in minutes
- **Length of Membership**: How many years the customer has been a member
- **Yearly Amount Spent**: Total amount spent by the customer in a year

## Setup and Installation

1. **Clone the repository**:
    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. **Install the necessary packages**:
    ```bash
    pip install numpy pandas matplotlib seaborn scikit-learn
    ```

3. **Load the dataset**:
    ```python
    import pandas as pd
    customers = pd.read_csv('Ecommerce Customers.csv')
    ```

## Exploratory Data Analysis (EDA)

- **Initial Data Inspection**:
    - Use `.head()`, `.info()`, and `.describe()` methods to understand the structure and summary statistics of the data.

- **Jointplot Analysis**:
    - Create jointplots to explore relationships between:
      - Time on Website vs. Yearly Amount Spent
      - Time on App vs. Yearly Amount Spent
      - Time on App vs. Length of Membership (using 2D hex bins)

- **Pairplot Analysis**:
    - Use `sns.pairplot()` to visualize relationships across all numerical features.

- **Heatmap Correlation**:
    - Generate a heatmap to see correlations between features.

- **Linear Model Plot**:
    - Create a linear model plot for Yearly Amount Spent vs. Length of Membership.

## Modeling

1. **Feature Selection**:
    - Select the numerical features: `Avg. Session Length`, `Time on App`, `Time on Website`, and `Length of Membership`.

2. **Data Splitting**:
    - Split the data into training and testing sets using `train_test_split` from `sklearn.model_selection`.

3. **Model Training**:
    - Train a `LinearRegression` model on the training data.

4. **Model Coefficients**:
    - Extract and inspect the model coefficients to understand the impact of each feature.

## Model Evaluation

- **Prediction**:
    - Use the trained model to predict values for the test set.
    - Create a scatterplot of the real vs. predicted values.

- **Error Metrics**:
    - Calculate the Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE) to evaluate model performance.

- **Residuals Analysis**:
    - Plot a histogram of the residuals to ensure they are normally distributed.

## Conclusion

The analysis reveals that:

- **Time on App** has a stronger correlation with Yearly Amount Spent compared to **Time on Website**.
- The most significant predictor of Yearly Amount Spent is the **Length of Membership**.

### Recommendation

The company should consider focusing more on improving the mobile app experience, but should not neglect the website, as there is still room for optimization. Additionally, strategies to increase membership duration could be beneficial.

## Next Steps

- Conduct further analysis after improving the website to reassess its impact.
- Explore other models or techniques to improve prediction accuracy.
