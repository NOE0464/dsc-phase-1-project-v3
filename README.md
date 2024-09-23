# Aircraft Acquisition Strategy

### Executive Summary
-Brief overview of the Business problem & Objectives

## Business Understanding
**PROBLEM STATEMENT**; The  Company has neither history nor experience in Travel industry ie(Aviation industry),determining which Aircraft will have lowest to none risk to start this new business endeavor at reasonable cost and succesful entry to the market
**Key Stakeholders**: Internal{Company stakeholders,potential investors}; External{government policies,competition(other airline businesses),customers}
**Responsibilty**: Business Analysts,key stakeholders
**Success Criteria**: succesful entry to the aviation industry with completion of regularites & selection of low risk aircraft
**Resources**: Budget, information on aircraft safety, Industry Reports,expert consultations
**Risks**:potential financial losses, safety incidents

### Project Plans & Goals
-Use provided **dataset** and available information inlets to have a general overview of the lifeline of Aviation Industry(requirements,advantages,disadvantages)
-Identifying main causes of accidents ,which aircraft is more prone to accidents?,are the  accidents due to human intervention?,are the aircrafts well maintained?.

## Data Analysis
### Part 1: data understanding
-The base outline of this project was provided by **Kaggle**,the initial findings was provided by another group of data analysts
-The findings of this project has been provided in **csv(Comma Separated Value) format** and stored in the **data file**under the name **Aviation_Data.csv**which basically outlines a range of aircraft& airline accidents
-The csv file is then read into a dataframe to allow 'surgery' of the information we want to get insights.
-The **dataframe** has **(90348=rows, 31=columns)** 
columns= unique field names
rows= have the unique figures of each column
-The **dataFrame** has both instances of **continous&categorical data**this becomes known after running{**df.info**}
continuos data = **float**(Qantitive)(measurable values representing a range of information)
categorical data = **object**(Qualitative)(not inform of numbers)

### Part 2 :Data Cleaning
-After getting to understand our data ,we have to dig further to know what is required&why for our project.
-The importance of this , is to get into the market with **clear,extensive and relevant knowledge** to get into the market
-1) We indentified if there was any missing row in our dataFrame,which to our understanding there was none
-2) Then identifying the total number {in %} of  values missing in all columns.This provides a basis on each column and their relevance to provide key insights to our project
-3)Deciding on a passmark of {60%} which of the columns are not relevant to our study;
"Longitude", "Latitude", "Location"- Tableau provides detailed axis points
"Schedule" - has more than 85% missing values 
"Air.Carrier"- has more than 80% missing values
"FAR Description"- necessary airline regulations that are incomplete and change fro time to time
Columns dropped on a passmark of over(40%)"Airport.Name"- do not add value since we aleady have **airport.codes** that provide a specific entry unlike names where you can have them to be the same
- Next we dropped all the rows with missing values
**identifying outliers** {continuos data} the outliers inthis case were just identified and ignored , since they might be used for future reference 
-Finally we decided to fill the mossing values of the continuos data whith it's own **median**
Median - is less sensitive to outliers than mean, preferred when the data distribution is skewed
