# Network_Distribution_Prediction
This project is from kaggle https://www.kaggle.com/c/telstra-recruiting-network

## Business Objective
A telecom company is interested in developing an advanced predictive model to
predict service disruptions based on the log files generated by multiple devices.
We have to output a csv file that can be handed to the operations team so they
can priorities dispatch of technicians based on fault_severity prediction and its
probability.

## Data Understanding
The data set is in a relational format, split among multiple
files. The following provides a description of data in each
file.

## Data Preparation
▪ Step 1: Import Modules
▪ Step 2: Import Datasets
Each row in the main dataset (train.csv, test.csv) represents a location and a time point. They are identified by the
"id" column, which is the key "id" used in other data files. Fault severity has 3 categories: 0,1,2 (0 meaning no
fault, 1 meaning only a few, and 2 meaning many). “fault_severity” is a measurement of actual reported faults
from users of the network and is the target variable (in train.csv). 

• Step 3: Data preprocessing
• Step 4: Data merging to create a single record (CAR)

• Step 5: Remove text from variables
Features are extracted from log files and other sources:
event_type.csv, log_feature.csv, resource_type.csv,
severity_type.csv. All above features are categorical except for
"volume".

• Step 6: Drop ”fault_severity” from train dataset as it is
the target variable

• Step 7: Merge the train dataframe without the
“fault_severity” column and the combined dataframe of
“event_type … etc”

• Step 8: Create dummy variables
• Step 9: groupby “id”

## Modeling
Algorithm Selection
A wide class of models can be used for Network Disruption Prediction
▪ Logistic Regression
▪ Random Forest
▪ Gradient Boosting
▪ K-Nearest Neighbors
▪ Decision Trees
Among Ensemble Methods, we have chosen Gradient Boosting Classifier because generally its
better performance. 

## Gradient Boosting Algorithm
The overall parameters can be divided into 3 categories:
§ Tree-Specific Parameters: These affect each individual tree in the model
Min_samples_split, min_samples_leaf, min_weight_fraction_leaf,
max_depth, max_leaf_nodes, max_features
§ Boosting Parameters: These affect the boosting operation in the model
Learning_rate, n_estimators, subsample
§ Miscellaneous Parameters: Other parameters for overall functioning
Loss, init, random_state, verbose, warm_start, presort
