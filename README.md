Traffic Analysis Using Machine Learning
This project utilizes machine learning techniques to analyze network traffic, identifying benign and malicious packets, specifically detecting brute-force attempts over SSH and FTP protocols. The dataset used is sourced from CICFlowMeter, providing a basis for network-based intrusion detection.

Dataset
The dataset, .csv, was obtained from the CICFlowMeter repository. It contains labeled traffic data, which includes both benign traffic and brute-force attack attempts.

Project Workflow
Data Preprocessing:

Import dataset using Pandas.
Perform label encoding for categorical values in the 'Label' column: mapping benign to 2 and brute-force attacks to 4.
Drop unnecessary columns to simplify the dataset and reduce feature space.
Feature Engineering:

Select relevant features for classification and convert appropriate columns to integer types.
Check and report missing values for each feature.
Data Balancing:

Extract and balance a subset of benign and malicious data for comparison.
Visualization:

Scatter plot visualizations for selected traffic protocols to understand class distribution.
Modeling:

Prepare independent (X) and dependent (y) variables.
Split the data into training and testing sets (80% train, 20% test).
Use an SVM (Support Vector Machine) model with a linear kernel for binary classification.
Evaluation:

Predict on test data and evaluate the model's performance.
Dependencies
Python 3.x
Pandas
NumPy
Matplotlib
Scikit-learn
To install the necessary dependencies, you can use the following command:

bash
Copy code
pip install pandas numpy matplotlib scikit-learn
Getting Started
Clone the Repository:

bash
Copy code
git clone <repository-url>
cd traffic-analysis-ml
Run the Notebook: Load and run the Jupyter notebook or Python script to see the preprocessing, feature engineering, and model evaluation steps.

Connect to Google Drive: Ensure Google Colab access if running on Colab and mount your Google Drive to access the dataset.

Train and Test: Modify the test_size parameter in the train-test split for experiments with data splits.

Results and Observations
The SVM model demonstrated the capability to distinguish between benign and brute-force network traffic. Future improvements may involve:

Testing alternative classifiers for improved accuracy.
Enhancing feature engineering and selection.
Expanding the dataset for generalization.
