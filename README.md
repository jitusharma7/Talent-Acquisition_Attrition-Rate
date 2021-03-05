# Talent-Acquisition_Attrition-Rate
The aim of project is to build a higher accurate model and  identify the key factors which are main driving factor for attrition rate.

## Table of Content
  * [Overview](#Overview)
  * [Problem_Definition](#Problem_Definition)
  * [Dataset_Description](#Dataset_Description)
  * [Exploratory_Data_Analysis](#Exploratory_Data_Analysis)
  * [Data_Preprocessing](#Data_Preprocessing)
  * [Model_Building](#Model_Building)
  * [Result](#Result)
  * [Business_Recommendation](#Business_Recommendation)
  * [Credit](#Credit)
  
## Overview
An attrition rate is a metric used to measure employees or customers lost over a period of time who are not replaced. The rate is shown as a percentage compared to the total workforce or customer base. Human resources employees often use an attrition rate to determine the number of vacant or eliminated positions

**Impact of attrition on Business**
The costs of employee attrition range from quantifiable numbers to hidden costs. When employees resign from companies, costs are incurred in recruiting new employees and training them. Productivity will be lower until new hires learn the business. If it is a customer-based business, customers could be dissatisfied if the new hire is not proficient.
 According to Deloitte, the average cost-per-hire is $4,000. This cost can be vary by country,region,industry,
 
 So attrition is vital metric and need to build suitable model and identify what are the key factor which drive individual to leave the organization.
 
 ## Problem_Definition
 One talent acquisition agency is facing challenges about default rate where candidates not joining the company after accepting the offer.Acquiring new talent is always a challenging and time-consuming task, especially in the IT industry since the recruit has to handle numerous changes in an ever-changing landscape. In many instances, it is even difficult to find the exact matching candidates for the specified job role. In such a scenario, if an offer is denied, then the human resource (HR) department has to repeat the entire recruitment process resulting in additional effort from the top management.
 
 The talent acquisition agency  is trying to address this problem by identifying patterns in their existing candidate records using Machine learning algorithm
 
 
 ## Dataset_Description
 The dataset consists of the following attributes:

* SLNO
* Candidate Ref - unique candidate reference number
* DOJ Extended
* Duration to accept offer 
* Notice period
* Offered band 
* Pecent hike expected in CTC
* Percent difference CTC
* Joining Bonus (1: yes, 0: No)
* Candidate relocate actual (1: yes, 0: No)
* Gender ( 1: Male, 0 : Female )
* Candidate Source
* Location
* Age
* Target Variable - Status ( 1 : Joined Organization , 0 : Not Joined Orgainization ) 

 
## Exploratory_Data_Analysis
* Among those who have not joined,only 11.89% are through employee referral program

  <img src="/source.PNG" width="300">

* Among those who have not joined,only 16.74% are female. It meansfemales are more likely to join

 <img src="/Gender.PNG" width="300">      
      
* Average hike offered to people whohave not joined is lesser than for peoplewho have joined

    <img src="/salary.PNG" width="300">
        
* Notice period and Duration to acceptoffer and slightly positive correlated.The possible reason could be , theymight be looking out for other jobs

     
     <img src="/Multicolinearity.PNG" width="500">



## Data_Preprocessing
* Encoding the Status column as 1and 0
* Dropping three features 'SLNO','Candidate Ref' and 'Location' dueto high cardinality
* Applying Label Encoding to'offered band' ordinal feature.
* Applying one hot encoding to restof the categorical features
* Used drop_first feature of one hotencoding to avoidmulticollinearity
* Checked for multicollinearity using correlation mapand variance Inflation factor,Two features 'Pecent hike expected in CTC' and'Percent hike offered in CTC' has been removed

    <img src="/VIF.PNG" width="400">






