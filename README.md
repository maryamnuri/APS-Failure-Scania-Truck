# APS Failure In Scania Trucks



### 1. Description

The dataset consists of data collected from heavy Scania trucks in everyday usage. The system in focus is the Air Pressure system (APS) which generates pressurised air that are utilized in various functions in a truck, such as braking and gear changes. The datasets' positive class consists of component failures for a specific component of the APS system. The negative class consists of trucks with failures for components not related to the APS. The data consists of a subset of all available data, selected by experts.

Positive class: Components failures for a specific component of the APS system (type 1)
Negative class: Failures for components not related to the APS (type 2)

The total cost of a prediction model the sum of Cost_1 multiplied by the number of Instances with type 1 failure and Cost_2 with the number of instances with type 2 failure, resulting in a Total_cost. In this case Cost_1 refers to the cost that an unnecessary check needs to be done by an mechanic at an workshop, while Cost_2 refer to the cost of missing a faulty truck, which may cause a breakdown. Cost_1 = 10 and Cost_2 = 500, and ,
Total_cost = Cost_1 No_Instances + Cost_2 No_Instances.


### 2. Problem Statement
To predict APS failure accurately and minimizes the cost of failures

### 3. Data
Refer: https://archive.ics.uci.edu/ml/datasets/APS+Failure+at+Scania+Trucks
2 data files:
train data: aps_failure_training_set.csv
test data: aps_failure_test_set.csv

### 4. Challenge Metric

     Cost-metric of miss-classification:

     Predicted class |      True class       |
                     |    pos    |    neg    |
     -----------------------------------------
      pos            |     -     |  Cost_1   |
     -----------------------------------------
      neg            |  Cost_2   |     -     |
     -----------------------------------------
     Cost_1 = 10 and cost_2 = 500
     
#### Checklist

#Checklist 1: Exploratory data analysis (EDA)
- [x] Visualise class label distribution
- [x] Missing/null values

#Checklist 2: Data Preprocessing
- [x] Handling missing values
- [x] Converting class label
- [x] Standardisation/Normalisation if needed
- [x] Feature selection (using RFE)
- [x] Handling imbalanced data using SMOTE

#Checklist 3: Researching for the best model
- [ ] Logistic Regression
- [x] Random Forest Classifier
- [x] XgBoost Classifier
- [ ] SVM

#Checklist 4: Model performance and Challenge Metric
- [x] f-1 score
- [x] Total cost for each models

