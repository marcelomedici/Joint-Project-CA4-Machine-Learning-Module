PROJECT SUMMARY:
- The project has the goal to create a ML models that can be replicable in similar scenarios to predict the billing category (Low, High) taking into consideration more than 5 thousads patient records.

Dataset Description: 
- 
The dataset originally contained 55,500 rows representing individual patient records and 15 columns, capturing various patient details, including Name, Age, Gender, Blood Type, Medical Condition, Date of Admission, Doctor, Hospital, Insurance Provider, Billing Amount, Room Number, Admission Type, Discharge Date, Medication, and Test Results.

Data Pre-Processing:



Vectorization Process:

1st Attempt: Vectorization: The first attempt led to high dimensionality due to using one-hot encoding to convert the text's categorical nominal data into numbers.
![image](https://github.com/user-attachments/assets/684648d2-4447-49ef-8052-01573810e695)

2nd Attempt: This is the final vectorization approach taken. Variables with a large number of categories were handled using label encoding to avoid an increase in dimensionality. For that reason, only a few categorical variables were one-hot encoded. During preprocessing, the Doctor and Hospital variables were removed. Even though they didn’t appear to have a significant impact, we retained some nominal categories as one-hot encoded to maintain a balance and avoid losing too much information from the dataset.
![image](https://github.com/user-attachments/assets/475ff56d-4fad-42eb-a473-7e1d724a3f79)



3nd Attempt:



Xgboost:














CODE PYTHON:
- Data Wrangling:
- Data Cleaning:
- Data Pre-processing:
- 
  
