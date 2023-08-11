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

## Summary
The results from the models shown above does not meet the requirement of an optimization above 75% accuracy.
The following steps were taken in order to try and achieve that requirement:
* increasing and decreasing number of inputs
* increasing and decreasing number of layers
* increasing and decreasing number of neurons per layer
* changing the activation type of the layers
* reducing epochs to the training regimen

 All models, including the ones shown, did not increase their accuracy above ~73% accuracy.  This could be due to the dataset needing further cleaning or conversion. 
 Another possible theory is that a satisfactory combination could not be achieved to meet the 75% accuracy requirement.  Perhaps using an auto-optimizer would yield better results.  
 However, there is a noticeable trend that the auto-optimizer prefers to use the "tanh" activation which could limit its capabilities.  

 ##Suggestion and Future Models
 If Alphabet Soup is satisfied with the 73% accuracy, it is recommended to use any of the models listed above.  However, to achieve abouve 75% accuracy, a larger-scale model could be used (more layers, neurons, and epochs).
 More time could also be spent researching on whether or not increasing neurons between hidden layers instead of lowering them yields better results.  A majority of the layers within the models listed above used the "relu" activation type.
 More experimentation on variation of activation types could yield a promising combination that could achieve a satisfactory accuracy score.
