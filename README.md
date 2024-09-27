## Heart_Disease_Prediction

The data set for this project (heart.csv) contains 4000 records and 16 variables. These 16 variables describe each participant of this study. The goal of this project is to generate a logistic regression model to predict whether coronary heart disease would occur within 10 years given such variables. This data set contains following variables:

Demographic:
1.	Sex of a participant male or female. 0-female. 1-male
2.	Age. This variable is expressed in whole numbers
3.	Education
   
Behavioral:
1.	currentSmoker. 0-non-smoker, 1-smoker
2.	cigsPerDay. This variable describes the number of cigarettes per day. Interval 0-20
   
Medical history:
1.	BPmeds: whether or not the patient was on blood pressure medication, 0-no, 1-yes
2.	prevalentStroke: whether or not the patient had previously had a stroke, 0-no, 1-yes
3.	prevalentHyp: whether or not the patient was hypertensive, 0-no, 1-yes
4.	diabetes: whether or not the patient had diabetes, 0-no, 1-yes
   
Medical(current):
1.	totChol:total cholesterol level
2.	sysBP: systolic blood pressure
3.	diaBP: diastolic blood pressure
4.	BMI: Body Mass Index
5.	heartrate: heart rate
6.	glucose: glucose level
   
Predictor variable: TenYearCHD: wether the coronary heart disease occurred within 10 years. 1 yes, 0-no

Model performance with default threshold (0.05) was poor:

              precision    recall  f1-score   support

           0       0.86      0.99      0.92       795
           1       0.65      0.09      0.16       143
    accuracy                           0.85       938


Model performance was greatly improved using the best threshold obtained from ROC curve (0.14):

              precision    recall  f1-score   support

           0       0.93      0.64      0.76       795
           1       0.27      0.73      0.39       143
    accuracy                           0.65       938


Conclusion: Using the best threshold obtained from ROC curve greatly improved the model performance in terms of
heart disease prediction:
default threshold (0.5): recall(0)=0.99 recall(1)=0.09
the best threshold(0.14): recall(0)=0.64 recall(1)=0.73
0-no heart disease 1-heart disease
