# A Machine Learning Project To Predict Blight Compliance

### A Binary Classifier Optimized for maximum Area Under Receiver Operating Characteristic Curve (AU-ROC Curve):
>  From Data Cleaning to Model Validation, Classifying whether a blight ticket will be paid in time or not, Trained 3 different Classifier on a Highly imbalanced Data provided by Detroit Open Data Portal with around 160000 Tickets.
## About The Data :

#### All The data for this project has been gathered through the Detroit Open Data Portal.

- *[Detroit Open Data Portal (Blight Violation)](https://data.detroitmi.gov/datasets/blight-violations)*

#### Description and More About Data Fields can found Here
 - [Descripton and Data Fields](https://github.com/ITrustNumbers/A_Classification_Model_To_Predict_Blight_Compliance/tree/master/Orignal_DataSet)
 
## Data Cleaning : ([Data Cleaning & Feature Engineering Notebook](https://github.com/ITrustNumbers/A_Classification_Model_To_Predict_Blight_Compliance/blob/master/Data%20Cleaning%20and%20Feature%20Engineering.ipynb))

1. **There are not a lot of null values in the data sets therefore, I Simply Dropped the rows with missing data and dropped *'violation_zip_code'* , *'non_us_str_zip_code'* , *'grafitti status'* Data Field as it was more than 60% missing, And i Also Dropped *'payement_date'* , *'collection_status'* Data Field to Avoid Data Leakage.**

![Missing Values Plot](https://github.com/ITrustNumbers/A_Classification_Model_To_Predict_Blight_Compliance/blob/master/Visualizations/Null_Values.png)

2. **Then, I Combined the lat-lon.csv and addresses.csv Data Set to the train.csv to Map each *ticket_id* to corresponding *Latitude & Longitude*.** 

3. **Cleaned up Some of the Text Based Error in the Data Set and Some Dissimilarities were Handeled**
     > - E.x : Some Data Fields were Filled with *'Deter'* & *'Determi'* instead of *'Determination'*

## Feature Engineering : ([Data Cleaning & Feature Engineering Notebook](https://github.com/ITrustNumbers/A_Classification_Model_To_Predict_Blight_Compliance/blob/master/Data%20Cleaning%20and%20Feature%20Engineering.ipynb))

1. **Use Several Data Fields To Extract Model Ready Information :** 
    > 'Disposition' ----> 'Responsible_by' & 'Fine_Waived' <br /> 'Violator_description' ----> 'Len_Description' & 'Count_Violation' <br /> 'VIolator_name' ----> 'Type of violator' <br /> 'Ticket_Issued_date' ----> 'Month_BIn' & 'Ticket_TIme'
2. **Categorical Data Was Mapped for EDA**
<br />

![Mapping](https://github.com/ITrustNumbers/A_Classification_Model_To_Predict_Blight_Compliance/blob/master/_Images/maping.png)
    
## Exploratory Data Analysis : ([EDA & Feature Selection Notebook](https://github.com/ITrustNumbers/A_Classification_Model_To_Predict_Blight_Compliance/blob/master/Exploratory%20Data%20Analysis%20%26%20Feature%20Selection.ipynb))

> 

**1. Categorical Feature Distribution :**
<br />

![Categorical Feature Distribution ](https://github.com/ITrustNumbers/A_Classification_Model_To_Predict_Blight_Compliance/blob/master/Visualizations/Categorical_Distribution.png)

<br />
<br />

**2. Categorical Feature Distribution  Over Compliance :**
<br />

![Categorical Feature Distribution Over Compliance](https://github.com/ITrustNumbers/A_Classification_Model_To_Predict_Blight_Compliance/blob/master/Visualizations/Compliance_Dist_Featue.png)
  
**3. Co-Relation Visualization :**
<br />

![Co-Relation Visualization](https://github.com/ITrustNumbers/A_Classification_Model_To_Predict_Blight_Compliance/blob/master/Visualizations/Heatmap.png)
