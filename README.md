# Predicting Hospital Admission at Emergency Department Triage Using Machine Learning

This project aims to improve the workflows of Emergency Departments (ED) by predicting patient admissions using machine learning models. By accurately forecasting admissions, hospitals can better prioritize patients, allocate resources efficiently, and improve operational efficiency in handling crowded situations.

## Problem Statement

Emergency Departments around the world are often faced with overcrowding and long patient wait times, leading to delays in care and reduced patient outcomes. This project seeks to address this issue by using predictive modeling to assist in triage and resource allocation, helping hospitals make informed decisions about patient care.

## Dataset

The dataset used in this project contains information about patients' emergency department visits. It includes the following:

- **Total Records:** 560,486
- **Total Features:** 972

After preprocessing and feature engineering, dimensionality was reduced to improve the signal-to-noise ratio and enhance model performance.

## Machine Learning Models Used

We experimented with the following machine learning models to predict hospital admissions:

- **Logistic Regression**
- **Random Forest Classifier**
- **XGBoost Classifier**

### Features Engineered

Several preprocessing techniques were applied to the data:

- **Dimensionality Reduction:** To reduce the number of features and focus on the most important ones.
- **Missing Value Imputation:** To handle missing data effectively.
- **One-Hot Encoding:** For categorical variable transformation.
- **Feature Scaling:** To normalize the data and ensure that all features are on the same scale.

## Web Application

A simple and user-friendly web application has been developed to demonstrate the use of the machine learning model in real-time hospital admission prediction.

### Features of the Web Application:
- Healthcare professionals can input patient data.
- The app will provide an instant prediction of whether the patient will require hospital admission.
- The model runs in the background to ensure predictions are fast and reliable.

### Running the Web Application Locally

To run the web application locally, follow these steps:

1. Clone this repository:

    ```bash
    git clone https://github.com/DeveshPant18/Predicting_Hospital_Admission-Project-
    ```

2. Navigate to the project directory:

    ```bash
    cd Predicting_Hospital_Admission-Project-
    ```

3. Install the required Python libraries:

    ```bash
    pip install -r requirements.txt
    ```

4. Run the Streamlit application:

    ```bash
    streamlit run capstone_app.py
    ```

You should now be able to access the application in your browser at [http://localhost:8501](http://localhost:8501).

## Pre-trained Models

The pre-trained models used in this project are available in the `App/` directory of this repository. To use the models, follow these steps:

1. Ensure the models are in the `App/` folder in your project directory.
2. The models can be loaded directly within the application. Here's an example of how to load the models:

    ```python
    import pickle

    # Load the model
    with open('models/random_forest_model.pkl', 'rb') as f:
        rf_model = pickle.load(f)

    # Use the model for predictions
    prediction = rf_model.predict(input_data)
    ```

Make sure to load the appropriate model for your needs (`random_forest_model.pkl`, `logistic_regression_model.pkl`, or `xgboost_model.pkl`).

## Contributing

If you'd like to contribute to this project, feel free to fork the repository and submit a pull request with your improvements.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- Thank you to all the contributors and resources that helped with the development of this project.
- Special thanks to the dataset providers for making the data available for public use.

## Contact

For any questions or inquiries, please feel free to reach out via email or open an issue in the repository.
