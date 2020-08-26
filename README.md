# A Machine Learning Project To Predict Blight Compliance

## A Binary Classifier Optimized for maximum Area Under Receiver Operating Characteristic Curve (AU-ROC Curve):
>  From Data Cleaning to Model Validation, Classifying whether a blight ticket will be paid in time or not, Trained 3 different Classifier on a Highly imbalanced Data provided by Detroit Open Data Portal with around 160000 Tickets.
<br />

# About The Data :

## All The data for this project has been gathered through the Detroit Open Data Portal.

- *[Detroit Open Data Portal (Blight Violation)](https://data.detroitmi.gov/datasets/blight-violations)*
<br />

## Data Descriptions :

1 **Original/train.csv - The Training Set (All Tickets Issued between 2004-2011)** 
<br />

2 **Original/validation.csv - The Validation Set (All Tickets Issued between 2012-2016)**
<br />

3 **Original/addresses.csv - Mapping From Ticket ID to Addresses**
<br />

3 **Original/lat-lon.csv - Mapping  Addresses to Latitude and Longitude**
<br />

## Data Fields :

1 **train.csv & test.csv**

- ticket_id - unique identifier for tickets
- agency_name - Agency that issued the ticket
- inspector_name - Name of inspector that issued the ticket
- violator_name - Name of the person/organization that the ticket was issued to
- violation_street_number, violation_street_name, violation_zip_code - Address where the violation occurred
- mailing_address_str_number, mailing_address_str_name, city, state, zip_code, non_us_str_code, country - Mailing address of the violator
- ticket_issued_date - Date and time the ticket was issued
- hearing_date - Date and time the violator's hearing was scheduled
- violation_code, violation_description - Type of violation
- disposition - Judgment and judgement type
- fine_amount - Violation fine amount, excluding fees
- admin_fee - $20 fee assigned to responsible judgments
- state_fee - $10 fee assigned to responsible judgments
- late_fee - 10% fee assigned to responsible judgments
- discount_amount - discount applied, if any
- clean_up_cost - DPW clean-up or graffiti removal cost
- judgment_amount - Sum of all fines and fees
- grafitti_status - Flag for graffiti violations
- payment_amount - Amount paid, if any
- payment_date - Date payment was made, if it was received
- payment_status - Current payment status as of Feb 1 2017
- balance_due - Fines and fees still owed
- collection_status - Flag for payments in collections
- compliance [target variable for prediction] 
-  Null = Not responsible
    - 0 = Responsible, non-compliant
    - 1 = Responsible, compliant
- compliance_detail - More information on why each ticket was marked compliant or non-compliant
