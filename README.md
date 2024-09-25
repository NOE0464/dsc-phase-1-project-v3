# Aircraft Acquisition Strategy

### Executive Summary
-Brief overview of the Business problem & Objectives

## Business Understanding
**PROBLEM STATEMENT; The  Company has neither history nor experience in Travel industry ie(Aviation industry),determining which Aircraft will have lowest to none risk to start this new business endeavor at reasonable cost and succesful entry to the market.** 
 **Key Stakeholders**: Internal{Company stakeholders,potential investors}; External{government policies,competition(other airline businesses),customers}.
 **Responsibilty**: Business Analysts,key stakeholders.
 **Success Criteria**: succesful entry to the aviation industry with completion of regularites & selection of low risk aircraft.
 **Resources**: Budget, information on aircraft safety, Industry Reports,expert consultations.
 **Risks**:potential financial losses, safety incidents.

### Project Plans & Goals
-Use provided **dataset** and available information inlets to have a general overview of the lifeline of Aviation Industry(requirements,advantages,disadvantages,safety measures). 
 -Identifying main causes of accidents ,which aircraft is more prone to accidents?,are the  accidents due to human intervention?,are the aircrafts well maintained?.

## Data Analysis
### Part 1: data understanding
-The base outline of this project was provided by **Kaggle** ,the initial findings was provided by another group of data analysts
-The findings of this project has been provided in **csv(Comma Separated Value) format** and stored in the **data file** under the name **Aviation_Data.csv** which basically outlines a range of aircraft& airline accidents
-The csv file is then read into a dataframe to allow 'surgery' of the information we want to get insights.
-The **dataframe** has **(90348=rows, 31=columns)** 
 columns provide  unique field names, while 
 rows provide  unique figures of each column
 -The **dataFrame** has both instances of **continous & categorical data** this becomes known after running{**df.info**}. 
 continuos data = **float**(Qantitive)(measurable values representing a range of information).
categorical data = **object**(Qualitative)(not inform of numbers).

### Part 2 :Data Cleaning
-After  understanding the data ,finding  what is required& why is it necessary? for "Project goal fulfillment"
 -The importance of this , is to get into the market with **clear,extensive and relevant knowledge** to get into the market
 -1) All rows were present in the data.
 -2) Then identifying the total number  of  values missing in{%} all columns.This provides a basis on each column and their relevance to provide key insights to our project. 
 -3)Deciding on a passmark of {60%} which of the columns are not relevant to our study;
 "Longitude", "Latitude", "Location"- Tableau provides detailed axis points
 "Schedule" - has more than 85% missing values 
 "Air.Carrier"- has more than 80% missing values
 "FAR Description"- necessary airline regulations that are incomplete and change from time to time.
 -Columns dropped on a passmark of over(40%)"Airport.Name"- do not add value since  **airport.codes** provide a specific entry unlike names where you can have them to be the same.
 -Drop all the rows with missing values.
 **identifying outliers** {continuos data} the outliers inthis case were just identified and ignored , since they might be used for future reference.
 -Finally filling the missing values of the continuos data whith it's own **median**
 Median - is less sensitive to outliers than mean, preferred when the data distribution is skewed
 
### Part 3: Data Aggregation
- all relevant data to form a basis of  research
**.groupby()** is used to find if their is a relationship in the dataframe
-aggregation actually provides a better understanding  on what steps to take in the Aviation industry since it gives accurate continous data on the different aspects and relationships of the data.
-  refer back to the **BusinessUnderstanding**
 **Aircraft Category= helps  understand before starting the business venture which of the aircraft categories is most prone to accidents.**
 **Country = helps understand no. of accidents and how spread out they are . This analysis will also explain how other competions are handling the market.
 **Make&Model = this gives general oversight on which route to take when purchasing safe aircraft. 
 **Weather Conditon & Aircraft damage = "how spread is human error?" the minimal amount exposes humans.this will provide a basis for criteria for hiring potential employees once in the market.
 **Amateur.Built = directly diving into the market may prove to be strenous and might also discourage shareholders/potential investors .So comes the decision to seek cheaper alternatives, are the cheaper airplanes(amateur.built) safer ?.**
### Part 4 : Data Visualisations
-For the final stage of data analysis performing  **VISUAL ANALYSIS{"seeing is believing"}**,this is done to prove the findings
**Groupedbarchart-Country-this helps see where their is a succesful safety market and gauge other competitions on how they are fairing on in the market**-Henceforth Japan provides a safer yet very competitive market, meanwhile Haiti offers a dangerous yet open market.
 **Piechart-Amateur.Built- see the results of the cheaper option and see if it actually fairs on better than the expensive airlines ,this will help management make decision that might be better**-This information therefore states that incidents involving professionally manufactured aircraft tend to have a higher average number of fatal injuries but also more uninjured individuals than amateur-built aircraft.
 **Linegraphs-provide a clear insight on how many aircraft damages were actually natural**:they give emphasis{warning}of not taking necessary flight precautions due to weather.
 **Heatmap- this was used to  {Identify associations and relationships between variables,Measure the strength and direction of those relationships,Guide hypothesis testing and data visualization,Support regression analysis and detect multicollinearity,Interpret results} of the continuos data**
 **Countplots-In the context of aircraft, the make typically comes first, followed by the model,Visualizing general Frequency Distribution based on high number of accidents,helps quick decision making .
 **Purpose.of.Flight = who caused the most fatalities in the air industry?**
## conclusions
After creating all necessary visualisations further initiative on determining what factors can best help prepare for  aviation industry,ie; 
 **competition in the aviation sector, number of flight risks & accidents across differnt factors also their causes**.
 -For deeper understanding we have converted our **finalised cleaned data to excel format** to be used in  **Tableau to create a dashboard to display visual data to gain deeper insight.**   