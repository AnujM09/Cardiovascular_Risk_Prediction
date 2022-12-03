# Cardiovascular_Risk_Prediction


In the given problem statement, we were asked to determine whether the patient has a 10-year risk of developing coronary heart disease (CHD). To do this, we looked at the heart disease dataset. The data comes from an ongoing cardiovascular study of people living in the Massachusetts town of Framingham. Information about the patients is provided by the dataset. 3390 records and 17 characteristics are included. Risk factors include behavioural, medical, and demographic aspects. Our main objective is to determine if the person will be afflicted by a coronary heart condition or not, therefore we drew several insights from that dataset that helped us understand the weighting of each feature and how they are interrelated.


## Data Discription

### Demographic:
* Sex: Male or Female("M" or "F")
* Age: Age of the patient; (Continuous - Although the recorded ages have been truncated to whole numbers, the concept of age is continuous)
### Behavioral:
* is_smoking: Whether or not the patient is a current smoker ("YES" or "NO")
* Cigs Per Day: The number of cigarettes that the person smoked on average in one day.(can be considered continuous as one can have any number of cigarettes, even half a cigarette.)
### Medical (History):
* BP Meds: Whether or not the patient was on blood pressure medication (Nominal)
* Prevalent Stroke: whether or not the patient had previously had a stroke (Nominal)
* Prevalent Hyp: Whether or not the patient was hypertensive (Nominal)
* Diabetes: Whether or not the patient had diabetes (Nominal)
### Medical (Current):
* Tot Chol: Total cholesterol level (Continuous)
* Sys BP: Systolic blood pressure (Continuous)
* Dia BP: Diastolic blood pressure (Continuous)
* BMI: Body Mass Index (Continuous)
* Heart Rate: Heart rate (Continuous - In medical research, variables such as heart rate though infact discrete, yet are considered continuous because of large number of possible values.)
* Glucose: Glucose level (Continuous)
### Predict Variable (Desired Target):
10-year risk of coronary heart disease CHD (binary: “1”, means “Yes”, “0” means “No”) - DV


## Business use case of the Project : 
In the healthcare industry, let's imagine a machine learning (ML) system is requested to forecast the likelihood that a patient would acquire cardiovascular disease within the following year. An expected result from the model is a risk score that, if it is equal to or higher than a certain threshold, shows that the patient is at risk of developing cardiovascular disease; otherwise, it signals no risk.

# Project Flowchart:
1. first steps in preparing (Loading the depend Libraries and the data)
2. Clean-Up
    * Handling null values.
    * Handling duplicate values.
    * Removing Outliers.
3. Exploratory Data Analysis
4. Feature engineering
    * Feature encoding
    * Checking correlation for feature removal.
    * Checking the distribution of the data.
5. Pre processing of the data.
    * Dealing with class imbalance.
    * Splitting and scaling the data.
6. Model implementation


# Conclusion :
## EDA insights:
* 15.1% of the population in our dataset is at risk for cardiovascular disease, while 84.9% of the population is unaffected (TenYearCHD).
* Cardiovascular disease is more likely to affect persons between the ages of 51 and 63.
* We can't prove smoking causes heart disease since, as we can see from the count plot, there isn't much of a difference between these two groups, and our severe smoker, who smokes 70 cigarettes a day, doesn't have a ten-year risk.
* Approximately 2800 patients are safe, while 500 patients who have not yet experienced a stroke are at risk.
* We can see that there are more people without diabetes here, and 500 or so people without diabetes are at danger. And only a small percentage of persons with diabetes are at danger.
* Most people with normal cholesterol levels range from 210 to 280, while those at risk have cholesterol levels between 215 and 285; this is a small but perfectly normal difference.
* Most healthy individuals have a heart rate that ranges from 68 to 83, while those who are at risk have a heart rate that ranges from 68 to 84. which holds true for both risky and non-risky individuals.
* The average person smokes between 1 and 10 cigarettes per day, with a heart rate between 60 and 100.

## ML Model Results :
* The substantial class imbalance in the training set was addressed by the addition of synthetic data points, which changed the data distribution in the train and test sets. As a result, the large class imbalance in the train set and the mismatch in the data distribution between the train and test sets are to blame for the high performance of the train set models rather than overfitting.
* The testing set's ROCAUC score for SVC is 0.60.
* The testing set's ROCAUC score for logistic regression is 0.62.
* The testing set's ROCAUC score for DTC is 0.66.
* The testing set's ROCAUC score for KNN is 0.68.
* The testing set's ROCAUC score for Random Forest Classifier is 0.72.
* For each model, a classification report and a confusion matrix have been plotted.
