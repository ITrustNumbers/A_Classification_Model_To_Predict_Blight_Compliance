# A Machine Learning Project To Predict Blight Compliance

### A Binary Classifier Optimized for maximum Area Under Receiver Operating Characteristic Curve (AU-ROC Curve):
>  From Data Cleaning to Model Validation, Classifying whether a blight ticket will be paid in time or not, Trained 3 different Classifier on a Highly imbalanced Data provided by Detroit Open Data Portal with around 160000 Tickets.
## About The Data :

#### All The data for this project has been gathered through the Detroit Open Data Portal.

- *[Detroit Open Data Portal (Blight Violation)](https://data.detroitmi.gov/datasets/blight-violations)*

#### Description and More About Data Fields can found Here
 - [Descripton and Data Fields](https://github.com/ITrustNumbers/A_Classification_Model_To_Predict_Blight_Compliance/tree/master/Orignal_DataSet)
 
## Data Cleaning :
1 There are not a lot of null values in the data sets therefore, I Simply Dropped the rows with missing data and dropped *'violation_zip_code'* , *'non_us_str_zip_code'* , *'grafitti status'* Data Field as it was more than 60% missing, And i Also Dropped *'payement_date'* , *'collection_status'* Data Field to Avoid Data Leakage.

- ![Missing Values Plot](https://github.com/ITrustNumbers/A_Classification_Model_To_Predict_Blight_Compliance/blob/master/Visualizations/Null_Values.png)



