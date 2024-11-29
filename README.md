Anemia Diagnosis Using Ensemble Learning and Explainable AI
Project Overview
This project focuses on building and analyzing machine learning models for diagnosing anemia using a dataset containing pixel intensities of red, green, and blue colors, along with hemoglobin (Hb) levels and anemia status. Several ensemble learning techniques (Bagging, Boosting, Stacking, and Voting) were implemented and evaluated. Additionally, explainable AI methods such as SHAP and LIME were used to interpret the models' decisions and provide insights into feature importance.

Dataset Description
The dataset includes the following features:

%Red Pixel, %Green Pixel, %Blue Pixel: Pixel intensities for RGB colors.
Hb (Hemoglobin): Measured hemoglobin levels.
Sex: Gender of the subject (M/F).
Anaemic: Target variable (Yes/No indicating anemia).
The dataset consists of 104 samples with a balanced representation of the target variable.

Objectives
Implement ensemble learning techniques (Bagging, Boosting, Stacking, and Voting).
Compare the performance of the models using accuracy, precision, recall, and F1 score.
Use Explainable AI (SHAP and LIME) to interpret model predictions and identify the most influential features.
Visualize insights through plots and graphs for feature analysis and model evaluation.
Methodology
1. Data Preprocessing
Handled missing values, if any, and encoded categorical features like "Sex."
Normalized the pixel intensity values for better model performance.
2. Ensemble Learning Models
Bagging
Implemented Random Forest as a Bagging technique to reduce variance.
Boosting
Used XGBoost to improve weak learners and minimize bias.
Stacking
Combined two base models (Random Forest and Logistic Regression) with a meta-model (Gradient Boosting).
Voting
Built hard and soft voting classifiers using Decision Tree, Random Forest, and XGBoost.
3. Cross-Validation
Performed k-fold cross-validation to evaluate the robustness of each model.
4. Explainable AI (XAI)
SHAP: Visualized the impact of features on individual predictions for the best-performing model.
LIME: Explained predictions for selected test instances.
Key Results
Feature Importance:

Hemoglobin (Hb) emerged as the most significant feature across models.
RGB pixel intensities contributed less significantly but added some predictive value.
Performance Metrics:

Boosting (XGBoost) outperformed other models with the highest accuracy, recall, and F1 score.
Bagging (Random Forest) achieved competitive performance and robust predictions.
Visualization Insights:

Correlation heatmaps revealed strong relationships between Hb and anemia status.
Pair plots highlighted class separability based on Hb and pixel features.
Calibration curves demonstrated the probability prediction accuracy of the models.
Visualizations
The project includes the following visualizations:

Correlation Heatmap: Showcases the relationship between features.
Pair Plot: Highlights feature distributions and separations between classes.
Learning Curves: Illustrates the performance of models with increasing training sizes.
Calibration Curves: Assesses probability prediction calibration.
Feature Importance: Displays the significance of features for Random Forest and XGBoost.
SHAP and LIME Outputs: Explains individual and overall feature impact on predictions.
Tools and Libraries Used
Programming Language: Python
Libraries:
Data Manipulation: pandas, numpy
Visualization: matplotlib, seaborn, shap, lime
Machine Learning: scikit-learn, xgboost
How to Run
Clone this repository.
Install the required libraries listed in requirements.txt.
Open the Jupyter Notebook or Python script provided.
Execute the cells step by step to preprocess the data, train models, evaluate performance, and generate visualizations.
Conclusion
This project demonstrates the effectiveness of ensemble learning models in diagnosing anemia with high accuracy. The use of XAI techniques adds transparency to model predictions, making the system reliable for medical decision-making. Hemoglobin levels were confirmed as the most critical feature, aligning with medical knowledge.

For further exploration, additional features or external datasets can be integrated to enhance prediction accuracy and generalizability.

