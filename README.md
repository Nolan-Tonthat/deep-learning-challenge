# Deep-Learning-Challenge
## Neural Network Model for Alphabet Soup: Predicting Success of Applicants After Hypothetical Funding

## Overview

This neural network model was created to help the nonprofit foundation Alphabet Soup select applicants for funding with the best chance of success in their ventures.
By using the end accuracy score of the model, we can determine whether or not the model can accurately predict if an organization is successful.

## Data Preprocessing
From preprocessing the CSV provided by Alphabet Soup, the following information emerged:
* Target variable is the column `"IS_SUCCESSFUL"`
  * data inside the column is binary (0 or 1) which can be referred to as yes or no
* Removed columns "EIN" and "NAME" from original dataframe
  * "EIN" and "NAME" are not target/feature columns so they do not provide anything towards the NN model.  Therefore, they are removed to prevent any confusion
* Feature variables are the remaining columns: `"APPLICATION_TYPE"`	`"AFFILIATION"`	`"CLASSIFICATION"`	`"USE_CASE"`	`"ORGANIZATION"`	`"STATUS"`	`"INCOME_AMT"`	`"SPECIAL_CONSIDERATIONS"`	`"ASK_AMT "` 

## Model Results

### Model 1: 3 Layers, 44 inputs
#### Accuracy: 0.730, Loss: 0.559
| Layer    | Neurons | Activation |
| :--------: | :-------: | :----------: |
| First | 44 | relu  |
| Second | 22 | relu  |
| Output | 1 | sigmoid  |

### Model 2: 6 Layers, 44 inputs
#### Accuracy: , Loss: 
| Layer    | Neurons | Activation |
| :--------: | :-------: | :----------: |
| First | 44 | relu  |
| Second | 33 | relu  |
| Third | 22 | relu  |
| Fourth | 11 | tanh  |
| Fifth | 6 | tanh  |
| Output | 1 | tanh  |


### Model 3: 6 Layers, 49 inputs
#### Accuracy: , Loss: 
| Layer    | Neurons | Activation |
| :--------: | :-------: | :----------: |
| First | 49 | relu  |
| Second | 33 | relu  |
| Third | 14 | relu  |
| Fourth | 21 | relu  |
| Fifth | 7 | relu  |
| Output | 1 | sigmoid  |
