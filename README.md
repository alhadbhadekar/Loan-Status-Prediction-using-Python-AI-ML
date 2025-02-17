# Loan Status Prediction Using AI/ML

## Overview

This project implements a loan status prediction model using machine learning techniques in Python. The objective is to determine whether a person is eligible for a loan based on various features.

## Dataset

The dataset used for this project can be downloaded from Kaggle:

[Download dataset.csv](https://www.kaggle.com/datasets/ninzaami/loan-predication)

### About the Dataset

The dataset includes the following features:

- **Loan_ID**: Unique identifier for each loan application
- **Gender**: Gender of the applicant
- **Married**: Marital status
- **Dependents**: Number of dependents
- **Education**: Educational qualification
- **Self_Employed**: Employment status
- **ApplicantIncome**: Income of the applicant
- **CoapplicantIncome**: Income of the co-applicant
- **LoanAmount**: Amount of loan requested
- **Loan_Amount_Term**: Term of the loan in months
- **Credit_History**: Credit history of the applicant
- **Property_Area**: Area of the property
- **Loan_Status**: Indicates if the loan was approved (Y) or not (N)

## Dependencies

Ensure you have the following Python packages installed:

- numpy
- pandas
- seaborn
- scikit-learn

You can install the required packages using pip:

```bash
pip install numpy pandas seaborn scikit-learn
```

## Project Structure

The main code is contained in the `Loan Status Prediction.ipynb` Jupyter notebook, which includes:

1. **Data Loading**: Loading the dataset into a pandas DataFrame.
2. **Data Pre-processing**: Handling missing values, encoding categorical variables, and replacing specific values.
3. **Data Visualization**: Visualizing relationships between features and loan status.
4. **Train-Test Split**: Splitting the dataset into training and testing sets.
5. **Data Standardization**: Standardizing the data for better model performance.
6. **Model Training**: Training a Support Vector Machine (SVM) model.
7. **Model Evaluation**: Evaluating the model's performance using accuracy metrics.
8. **Prediction**: Testing the model with new input data.

## Getting Started

1. **Download the Dataset**: Make sure you have the `dataset.csv` file in your project directory.

2. **Run the Jupyter Notebook**: Open `Loan Status Prediction.ipynb` and execute the cells sequentially.

3. **Model Training and Evaluation**: The notebook includes code to train the model and evaluate its accuracy on both training and test datasets.

## Example Usage

After running the model, you can test predictions using new input data:

```python
input_data = (1, 1, 1, 1, 0, 4583, 1508.0, 128.0, 360.0, 1.0, 0)

# Changing the input data to a numpy array
input_data_as_numpy_array = np.asarray(input_data)

# Reshape the array as we are predicting for one instance
input_data_reshaped = input_data_as_numpy_array.reshape(1, -1)

# Standardize the input data
std_data = scaler.transform(input_data_reshaped)

# Predicting the loan eligibility
prediction = classifier.predict(std_data)

if (prediction[0] == 0):
    print('Person is not eligible to get Loan')
else:
    print('Person is eligible to get Loan')
```

## Acknowledgments

- Dataset from [Kaggle](https://www.kaggle.com/datasets/ninzaami/loan-predication)
- Seaborn for data visualization
- Scikit-learn for machine learning utilities

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


## Conclusion

This project provides a foundation for building AI/ML applications for loan prediction. Happy coding!