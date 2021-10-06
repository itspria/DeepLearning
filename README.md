# Charity Funding Predictor
A neural network model was created to predict whether the applicants funded by Alphabet Soup will be successful or not. The dataset obtained from Alphabet Soup's business team contains 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:
- EIN and NAME — Identification columns
- APPLICATION_TYPE — Alphabet Soup application type
- AFFILIATION — Affiliated sector of industry
- CLASSIFICATION — Government organization classification
- USE_CASE — Use case for funding
- ORGANIZATION — Organization type
- STATUS — Active status
- INCOME_AMT — Income classification
- SPECIAL_CONSIDERATIONS — Special consideration for application
- ASK_AMT — Funding amount requested
- IS_SUCCESSFUL — Was the money used effectively

## Data Preprocessing
The data from the csv file was loaded into pandas dataframe and transformed to be used in the model. The get_dummies function was used to encode categorical data. The dataset split into test and training data. The data was scaled with Scikit-Learn’s StandardScaler() to be used in the model.
- Targets
  - IS_SUCCESSFUL field was chosen as target
- Features
  - APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
- Ignored
  - EIN, NAME
  
## Compile, Train and Evaluate the Model
A neural network model was created using Tnsorflow Keras consisting of 2 hidden layers with relu activation and an outer layer with sigmoid. The model was fitted with the training data and run for 100 epochs. The test data was later used to evaluate the model and determine loss and accuracy

## Optimization
The model was optimized by increasing the layer, increasing the neurons in each layer, changing the activation function in each layer and increasing/decreasing the epoch

## Summary
The model only shows the accuracy of 73%. 
Changing various parameters didnot improve the accuracy greatly. 
More features in the dataset could help in training the data better.
