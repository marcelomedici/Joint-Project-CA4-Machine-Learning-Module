# Project---Police-Killings-Scenario-USA

Project CA1 Data Visualisation 

Title: Police Killings Scenario in USA

Description: The project aims to study the scenario of the deaths caused by Police's operation in United States of America between 2015 to 2017, investigating the patterns among the variables.

Content: The original file has been modified in some levels to match an better undertanding of the information. 

PYTHON CODE MODIFICATIONS:
1.  Columns such as "armed," "race," and "flee" were modified. N/A values were substituted with 'Not Specified.'
        1.1 df1['armed'].fillna('Not specified',inplace=True)
        1.2 df1['race'].fillna('Not specified', inplace=True)
        1.3 df1['flee'].fillna('Not specified', inplace=True)
         
2. The gaps in the "age" column was filled with N/A value.
        2.1 df1['age'].fillna(N/A, inplace=True)
            
3. "Body Camera" and "Signs_of_mental_illness" columns were modified from boolean to string, with 'Yes' and 'No' respectively.
        3.1 df1['body_camera'] = df1['body_camera'].replace({False:'No', True: 'Yes'})
        3.2 df1['signs_of_mental_illness'] = df1['signs_of_mental_illness'].replace({False:'No', True:'Yes'})

4. The "race" and "gender" columns were changed: abbreviations were replaced with full names.
        4.1 df1['race'].fillna('Not specified', inplace=True)
        4.2 df1['gender'] = df1['gender'].replace({'M': 'Male', 'F': 'Female'})

5. The "date" column datatype was changed to date format ('%d/%m/%Y').
        5.1 df1['date'] = pd.to_datetime(df1['date'], format='%d/%m/%Y', errors='coerce')

6. Values in the collumn 'gender' have been modified from abbreviations to full name aiming for easier readabiity.
        6.1 df1['gender'] = df1['gender'].replace({'M': 'Male', 'F': 'Female'})


7. Values in the collumn 'race' have been modified from abbreviations to full name aiming for easier readabiity.
        7.1 df1['race'] = df1['race'].replace({'A':'Asian','H':'Hispanic', 'B':'Black_African American', 'N': 'Native_Indigenous', 'O': 'Other', 'W': 'White_Caucasian'})
   
   ***Ask to Lisa ABOUT the code changes regading the column 'ARMED' to add here***
        
POWER BI Query Changes:


***TABLEU Query Changes:***
              
              
              
              
              

              
Data Visualisation Proggrams: Power BI and Tableau 
