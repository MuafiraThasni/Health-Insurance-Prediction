# Health-Insurance-Prediction

People’s healthcare cost forecasting is now a valuable tool for improving healthcare accountability. The healthcare sector produces a very large amount of data related to patients, diseases, and diagnosis, but since it has not been analyzed properly, it does not provide the significance which it holds along with the patient healthcare cost.

For the webapp [click here](https://share.streamlit.io/muafirathasni/health-insurance-prediction/main/insurance_app.py)

**Dataset:** US Premium Health Insurance Charges : https://www.kaggle.com/teertha/ushealthinsurancedataset

**Project Objective:** study and understand the risk underwriting in Health Insurance, the interplay of various attributes of the insured and to see how they affect the insurance premium.

## Exploring the Data

<img src="/bmi_age_count.png?raw=true"/>


<img src="/categorical.png?raw=true"/>

When it comes to machine learning, feature engineering is the process of extracting features from raw data while applying domain expertise in order to improve the performance of ML algorithms. In the medical insurance cost dataset, attributes such as smoker, BMI, and age are the most important factors that determine charges. Also, we see that sex, children, and region do not affect much the charges

<img src="/heatmap.png?raw=true"/>


### Multi-variate Analysis

The BMI values of sex or gender types (male and female) are given in the x-axis, and the charges are presented in the y-axis. It can be clearly seen that when the values of BMI are varied, the insurance charges will vary accordingly 

<img src="/charge_bmi.png?raw=true"/>




<img src="/smoker_charge.png?raw=true"/>


## Modeling

* Linear Regression model is selected as baseline model. 
* Features considered are: bmi , children_0,smoker_yes, region_southeast, region_southwest, age_group_old, age_group_young
* Final R squared obtained for base model - 74.1%

The baseline model is improved again. First a decision tree regressor algorithms is used. The XGBoost algorithm is used to improve the model again. Final model is based on XG Boost algorithm and corresponding performance metrics are as given below:

* Accuracy score (training): 0.875
* Accuracy score (test): 0.898

Importance of features for the final model : 

<img src="/features.png?raw=true"/>

For Code, [see Notebook](https://github.com/MuafiraThasni/Health-Insurance-Prediction/blob/main/EDA%20%20and%20model%20building%20for%20premium%20insurance%20prediction.ipynb)
