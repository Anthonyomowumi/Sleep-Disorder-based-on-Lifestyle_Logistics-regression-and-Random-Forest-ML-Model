# About the Dataset
This Project is utilizing the Sleep Health and Lifestyle Dataset in Kaggle, A secondary Data. This is basically measuring the impart of someone's lifestyle on their health.
The Dataset contains 14 columns in total (That is, 13 features and 1 classification columns with 3 labels/category/mulitclass - None, Sleep Aspnea and Insomnia). The dataset contains 374 rows in total excluding the data header row

# Data Description
The 13 features includes; Person Identifier (ID), Gender (Male/Female), Age (In years), Occupation(Profession of the Person), Sleep duration (In hours per day), Quality of Sleep (On a scale rating 1-10 with 1- no significance,
5-medium significance and 9/10-high significance...It is a subjectice rating based on feelings and opinions), Physical Activity Level (In minutes per day, Stress Level (On a scale rating of 1-10, measure how stress level experienced 
by the Individual, it is also subjective rating),Systolic Blood Pressure in mmHg, Diastolic Blood Pressure in mmHg, Heart rate in bpm (Beat per minutes), Daily Steps (In count), 
The Classification Column is the SLEEP DISORDER COLUMN with 3 labels - None, Sleep Apnea and Insomnia.

<img width="916" alt="image" src="https://github.com/user-attachments/assets/643ada82-535a-43c7-ad2e-a425ecdd94c6">


# Aim of this Project
This study aimed at utilising logistics Regression and Randomforest to model the best predictors for determining what features affect the sleep health of some certain Professions based on their Lifestyle
and classifying the Sleep Disorder class.

# Some Techniques Used:
#### Class Imbalance Handling: The dataset was imbalanced, so I applied SMOTE after the train-test split to avoid data leakage. SMOTE was applied only to the training set to ensure realistic performance evaluation.
#### Stratified Splitting: I used stratify=y during the train-test split to maintain consistent class distribution across training and test sets, which is crucial for imbalanced datasets.
#### Feature Scaling: For Logistic Regression, I standardized the features as this method works best with this model. In contrast, Random Forest, being robust to feature scaling, was evaluated on both scaled and unscaled data to compare performance.

# Work Done - Model Building and Evaluation
A multiclass a logistics regression (LR) model and Random Forest (RF) Model was built. LR has an accuracy of 87% and RF has an accuracy of 83% on the test data while both has an overall AUC of 91% indicates that the models 
has a high ability to distinguish between classes and a feature importance intrepretation from RF Classifier Feature Importance score and Permutation Importance Feature Score for logistics model and RandomForest Classifier 
was used to get the features contributing to the predictions of the models (which is, the sleep disorders/target variables)

##### Random Forest: highlighted Systolic BP, Diastolic BP, BMI, Occupation, and Physical Activity as significant predictors of sleep disorders.
##### Lasso Regression: identified Quality of Sleep, Stress Level, and Gender as key factors.

These insights align with research linking sleep deprivation and hypertension, underscoring the complex relationship between high blood pressure and sleep disorders.

