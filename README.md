# Cardiovascular Disease Detection

## The Cardio Catch Diseases (CCD) Company
Cadio Catch Diseases is a company that specializes in detecting heart disease in the early stages. Its business model is Service type, that is, the company offers an early diagnosis of cardiovascular disease for a certain price.

Currently, the diagnosis of cardiovascular disease is made manually by a team of specialists. The current accuracy of the diagnosis varies between 55% and 65%, due to the complexity of the diagnosis and also the fatigue of the team who take turns to minimize the risks. The cost of each diagnosis, including the devices and the payroll of the analysts, is around BRL 1,000.00.

The price of the diagnosis, paid by the client, varies according to the precision achieved by the team of specialists, the client pays BRL 500.00 for every 5% accuracy above 50%. For example, for an accuracy of 55%, the diagnosis costs BRL 500.00 for the client, for an accuracy of 60%, the value is R BRL 1000.00 and so on. If the diagnostic accuracy is 50%, the customer does not pay for it.

Note that the variation in precision given by the team of specialists, makes the company either have a profitable operation, revenue greater than the cost, or an operation at a loss, revenue less than the cost. This instability of the diagnosis makes the company to have an unpredictable Cashflow.

Your objective as the Data Scientist hired by Cardio Catch Diseases is to create a tool that increases the accuracy of the diagnosis and that this accuracy is stable for all diagnoses.

So your job as a Data Scientist is to create a patient classification tool, such as stable accuracy. Along with the tool, you need to send a report to the CEO of Cardio Catch Diseases, reporting the results and answering the following questions: (He will probably ask these questions on the day of your presentation.)

What is the Accuracy and Precision of the tool? How much profit will Cardio Catch Diseases have with the new tool? How Reliable is the result given by the new tool? The Challenge Data The data set that will be used to create the solution for Cardio Catch Diseases, is available on the Kaggle platform.

This is the link: Cardiovascular Disease dataset

This data set contains 70,000 patient diagnoses. You will use this data to create your solution.

## Features Description
There are 3 types of input features:

Objective: factual information;
Examination: results of medical examination;
Subjective: information given by the patient.

Features:
- Age | Objective Feature | age | int (days)
- Height | Objective Feature | height | int (cm) |
- Weight | Objective Feature | weight | float (kg) |
- Gender | Objective Feature | gender | categorical code |
- Systolic blood pressure | Examination Feature | ap_hi | int |
- Diastolic blood pressure | Examination Feature | ap_lo | int |
- Cholesterol | Examination Feature | cholesterol | 1: normal, 2: above normal, 3: well above normal |
- Glucose | Examination Feature | gluc | 1: normal, 2: above normal, 3: well above normal |
- Smoking | Subjective Feature | smoke | binary |
- Alcohol intake | Subjective Feature | alco | binary |
- Physical activity | Subjective Feature | active | binary |
- Presence or absence of cardiovascular disease | Target Variable | cardio | binary |

All of the dataset values were collected at the moment of medical examination.

## BUSINESS PERFORMANCE

Manual diagnosis with precision between 55% and 65%.
Customer pays BRL 500.00 for each 5% precision above 50%, which means 500/5 = BRL 100 each 1% precision
Diagnosis with 50% precision - customer does not pay - Baseline
Diagnosis with 55% preecision - customer pays BRL 500.00. - WORST CASE
Diagnosis with 60% precision - customer pays BRL 1,000.00.
Diagnosis with 65% precision - customer pays BRL 1,500.00 - BEST CASE

### Model and Business Summary:

The LGBMClassifier genetared an average accuracy of 73.36% with stable performance;
The model has a precision of 74.88%, almost 10% improvement compared to the current manual analysis (65%);
Considering a 70,000 patients database, the revenue can reach up to R$ 169,680,000.00, almost 65 million more than the current revenue best case;
Even in the worst case scenario, the revenue can reach R$157,360,000.00 even 52 million reais more than the current best scenario;


## FUTURE CHALLENGES

Improvements for the next CRISP cycle:

- Deepen the treatment of outliers;
- Change rescaling application;
- Apply CatBoostClassifier model;
- Change threshold to improve recall;
- Create a Model Deployment and put the model into production;
- Collect more data for analysis
    Hypotheses for Future Analysis:
    
    1. People with a previous heart disease should have more cardio disease.
    2. People with a family history of heart disease should have more cardio disease.
    3. People with autoimmune diseases should have more cardio disease.
    4. People with psychological illnesses like anxiety and depression should have more cardio disease.
    5. People with triglycerides higher then 200mg/dL should have more cardio disease.
    6. People with glucose (fasting) higher then 125mg/dL should have more cardio disease.
    7. People who drink should have more cardio disease.
    8. People who eat healthily should have less cardio disease.
