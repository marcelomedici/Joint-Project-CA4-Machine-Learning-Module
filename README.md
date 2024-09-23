# Project---Police-Killings-Scenario-USA
Project CA1 Data Visualisation 
Title: Police Killings Scenario in USA
Description: The project aims to study the scenario of the deaths caused by Police's operation in United States of America between 2015 to 2017, investigating the patterns among the variables.
Content: The original file has been modified in some levels to match an better undertanding of the information. The changes below were applied;
        Columns such as "armed," "race," and "flee" were modified. N/A values were substituted with 'Not Specified.'
        The "age" column was modified, and N/A values were substituted with '0' to keep the column as numerical.
        "Body Camera" and "Signs_of_mental_illness" columns were modified from boolean to string, with 'Yes' and 'No' respectively.
        The "race" and "gender" columns were changed: abbreviations were replaced with full names.
        The "date" column datatype was changed to date format ('%d/%m/%Y').
Codes:
              df1['armed'].fillna('Not specified',inplace=True)
              df1['race'].fillna('Not specified', inplace=True)
              df1['flee'].fillna('Not specified', inplace=True)
              df1['age'].fillna(0, inplace=True)
              df1['body_camera'] = df1['body_camera'].replace({False:'No', True: 'Yes'})
              df1['gender'] = df1['gender'].replace({'M': 'Male', 'F': 'Female'})
              df1['signs_of_mental_illness'] = df1['signs_of_mental_illness'].replace({False:'No', True:'Yes'})
              df1['race'] = df1['race'].replace({'A':'Asian','H':'Hispanic', 'B':'Black_African American', 'N': 'Native_Indigenous', 'O': 'Other', 'W':       'White_Caucasian'})
Data Visualisation Proggrams: Power BI and Tableau 
