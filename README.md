# deep-learning-challenge
Module 21 Challenge for Data Analytics Boot Camp

# Overview
The purpose of this analysis is to analyze a prepared dataset of organizations that have received funding from the hypothetical Alphabet Soup organization to predict whether future applicants will be successful if they are funded by Alphabet Soup.

# Results
## Data Preprocessing
The target variable for this model is the IS_SUCCESSFUL column.

The features for this model are APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT columns.

The variables to be removed are the EIN and NAME columns, as these are used for identifying unique loans.

## Compiling, Training, and Evaluating the Model
The initial neural network model began with 43 features, and had two hidden layers with 80 and 30 neurons respectively that were activated using relu functions.  With above 34,000 rows of data across 43 features, I began with near double the number of neurons in the first hidden layer to gauge how near to the target accuracy of 75% that the model would be.  This first model was able to achieve an accuracy of 72.56%.

To increase performance, the second neural network model was trimmed down to 41 features, with three columns of income data greater than $5 million compressed into a single been, and two more hidden layers each with 50 neurons were added.  These values were selected as a middle-ground between the first hidden layer's 80 neurons and the last hidden layer's 30 neurons.  This increased the accuracy to 72.61%.

For the final attempt, a keras tuner was set up to establish hyperparameters to find the best possible set of number of hidden layers and neurons.  The max number of epochs was reduced to 30 epochs as well.  The model that was produced finished with an accuracy of 72.83%.  As such, the tuner was not able to meet the target model performance of 75% accuracy.

# Summary