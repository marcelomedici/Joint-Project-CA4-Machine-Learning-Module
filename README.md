PROJECT SUMMARY:
-
The project has the goal to create a ML models that can be replicable in similar scenarios to predict the billing category (Low, High) taking into consideration more than 5 thousads patient records.

Dataset Description: 
- 
The dataset originally contained 55,500 rows representing individual patient records and 15 columns, capturing various patient details, including Name, Age, Gender, Blood Type, Medical Condition, Date of Admission, Doctor, Hospital, Insurance Provider, Billing Amount, Room Number, Admission Type, Discharge Date, Medication, and Test Results.

Data Pre-Processing:
-
After feature engineering, we extracted useful information regarding the length of stay from the admission and discharge dates. This helped reduce dimensionality while retaining important information that can be used to predict the billing amount. A similar approach was taken with weekend stays, under the assumption that weekends may be linked to the final bill amount.

Considering this, during preprocessing, we removed the original columns used to create the engineered features due to their high correlation. We also deleted name columns, as they contain only patient-specific proper nouns and do not carry meaningful information for prediction.
![image](https://github.com/user-attachments/assets/a58473ee-b63e-49ca-bdca-8a18c0e60ac5)

Vectorization Process:
-
1st Attempt: Vectorization: The first attempt led to high dimensionality due to using one-hot encoding to convert the text's categorical nominal data into numbers.
![image](https://github.com/user-attachments/assets/684648d2-4447-49ef-8052-01573810e695)

2nd Attempt: This is the final vectorization approach taken. Variables with a large number of categories were handled using label encoding to avoid an increase in dimensionality. For that reason, only a few categorical variables were one-hot encoded. During preprocessing, the Doctor and Hospital variables were removed. Even though they didn’t appear to have a significant impact, we retained some nominal categories as one-hot encoded to maintain a balance and avoid losing too much information from the dataset.
![image](https://github.com/user-attachments/assets/475ff56d-4fad-42eb-a473-7e1d724a3f79)

Xgboost:
-
The model was implemented in a simple way. the first performance rate reached was: ROC-AUC: 0.5171
Test Accuracy: 0.5121285627653123. so the hyperparameter tuning was applied, which improved the results: Acurracy: 0.539963 / F1Score: 0.539959 / Combined Score: 0.5399 
![image](https://github.com/user-attachments/assets/313ba7a0-c4a4-4850-b658-b5a969703c8e)

![image](https://github.com/user-attachments/assets/d1e37ba7-fcdc-4df6-a77e-22868f20bddc)


Naives Bayes: 
-
The method was chosen due to its ease of application and interpretation. To apply it, I needed to rescale the numerical variables, as it cannot work with negative numbers—it makes assumptions based on probability. The model seemed to run smoothly, but for some reason, I couldn’t get the Random Search method to work without errors."
![image](https://github.com/user-attachments/assets/b02838ff-286e-49cd-8cb2-20ac9ab2f82b)


Individual contributions table:


















