# Sparkify Project Overview

## Introduction / Overview
Sparkify is a fictional streaming music service interested in predicting user churn—when users are likely to cancel their service. This project utilizes a comprehensive dataset of user activity to model churn prediction using Apache Spark, allowing for scalable data processing and machine learning model development.

You can visit the related blog post on medium for this project https://medium.com/@miguelguzman.tob/predicting-user-churn-using-sparks-ml-lib-at-sparkify-60fbe8b2c5a4

## Metrics
The provided dataset is imbalanced, therefore the measures used to determine the model's performance are precision, recall and f1-score.

## Dataset
The project uses two datasets:
- `mini_sparkify_event_data_full.json`: A complete dataset of 12GB containing the entirety of user events.
- `mini_sparkify_event_data.json`: A smaller subset of the dataset, used primarily for training the machine learning model.

## Files
- `Sparkify.ipynb`: A Jupyter Notebook containing all the code and analysis for the project.
- `mini_sparkify_event_data_full.json`: Full dataset (12GB) - Not provided on this repository.
- `mini_sparkify_event_data.json`: Subset used for model training - Not provided on this repository.

## Libraries Used
- PySpark: For data manipulation and model building.
- Matplotlib: For creating visualizations.
- Pandas: For data manipulation and analysis.

## Project Setup and Execution
1. Clone the repository to your local machine or cloud environment.
2. Ensure that Apache Spark is installed and correctly configured.
3. Launch the `Sparkify.ipynb` Jupyter Notebook in a Spark-enabled environment.
4. Run the notebook cells sequentially to preprocess the data, engineer features, train the model, and evaluate the results.

## Model Development
Using Spark MLlib, the project involves the following steps:
- Data preprocessing: Cleaning data and preparing features.
- Feature engineering: Creating relevant features for churn prediction.
- Model training and tuning: Building and optimizing a machine learning model to predict churn.

## Results and Conclusion

After completing the modeling process, we've developed a robust model capable of predicting user churn with high accuracy. The model achieves approximately 85% in accuracy, precision, and recall.

The solution involved several key steps:
- **Data Cleaning:** We defined a schema to clean the data effectively, including the removal of rows where user information was missing, as this data was not suitable for imputation.
- **Data Transformation:** User actions were aggregated into a "bag of events" format, which tallies each type of action a user takes within the app.
- **Model Training:** We tested several models using ML pipelines and selected the best-performing model for predicting user retention based on their app interactions.

Challenges encountered during the project included:
- Defining churn and processing user actions in a way that was suitable for machine learning analysis proved complex.
- Various visualizations were created to explore potential models and understand data patterns; however, these did not yield actionable insights or contribute significantly to model selection.

### Improvements
While the model performs well, there is noticeable performance degradation between the training and test datasets, potentially due to class imbalance. To address this:
- **Data Augmentation:** Incorporating more varied data from the test set or using synthetic data generation techniques like SMOTE might improve model generalization.
- **Performance Acceptance:** Given the constraints and current performance, the model is deemed sufficiently effective for this phase of the project. However, continuous monitoring and iterative improvements are recommended to enhance its predictive accuracy over time.

## Contact
For any additional questions or contributions to the project, please open an issue in this repository or submit a pull request.

Thank you for visiting the Sparkify project repository!
