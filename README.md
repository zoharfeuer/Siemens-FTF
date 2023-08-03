# Failure Analysis Project

## Introduction
This project generates and analyzes data related to equipment failures in an industrial setting. The data includes various attributes such as failure types, technicians' experience, and the number of days since the failure was opened. The generated data is then used to train a logistic regression model to predict whether a failure will be fixed or not, and a gradient boosting classifier to predict the number of visits required to fix a failure.

## Data Generation

The data is generated using Python, and it includes the following steps:

1. Create lists of failure IDs, failure types, and reasons for not fixing a failure.
2. Generate a normal distribution of the number of days since the failure was opened.
3. Simulate failure visits with random attributes such as visit date, technician ID, failure status before and after the visit, etc.
4. Add not fixed reasons to some failure visits based on probability distributions.

The generated data is saved to a CSV file named 'failure_data.csv'.

## Data Preprocessing

Before training the models, the data is preprocessed using Python. The following steps are performed:

1. Drop irrelevant columns such as 'failure_visit_id', 'visit_date', and 'failure_status_after_visit'.
2. Replace zero values in the 'years_of_experience' column with 1.
3. Fill missing values in various columns with the most common value in each column.
4. One-hot encode the categorical variables.

The preprocessed data is saved to a new CSV file named 'clean_data.csv'.

## Logistic Regression Model

The logistic regression model is trained using the clean data to predict whether a failure will be fixed or not. The following steps are performed:

1. Split the data into training and test sets.
2. Train the logistic regression model using the training data.
3. Evaluate the model's accuracy on the test data.

The model achieves an accuracy of approximately 86.38%.

## Gradient Boosting Classifier

The gradient boosting classifier is trained using the clean data to predict the number of visits required to fix a failure. The following steps are performed:

1. Split the data into training and test sets.
2. Train the gradient boosting classifier using the training data.
3. Evaluate the model's accuracy on the test data.

The model achieves an accuracy of approximately 99.16%.

## Visualization

These were made in a separate Tableau 

## Requirements

The following libraries are required to run this project:

- Pandas
- Numpy
- Scikit-learn
- Matplotlib
- ydata-profiling (for data profiling)

## How to Use

1. Clone the repository or download the project files.
2. Run the 'failure_analysis.py' script to generate the data, preprocess it, and train the models.
3. After running the script, you will have two CSV files: 'clean_data.csv' and 'final_pred.csv'.
4. The 'final_pred.csv' file contains the predictions made by the models.
5. To view the visualizations, run the 'visualization.py' script.

## Contributors

- [Your Name]

Feel free to contribute to this project by adding more features, improving the models, or enhancing the visualizations.

**Note:** This README assumes that you have Python and the required libraries installed. If not, please install them before running the scripts.

---
*This project is for educational purposes and simulated data. It does not represent real-world scenarios.*
