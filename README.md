# Overview of the analysis: 
To use the variables in the provided dataset to help the client create a binary classifier capable of predicting whether applicants will be successful if funded by Alphabet Soup. From Alphabet Soup’s business team, we received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are numerous columns that capture metadata about each organization.

# Purpose
To help the foundation predict where to make investments.

# Results:
## Data Preprocessing
#### Target for the model
The target of the analysis is to ascertain whether the investments are successful. In our dataset, it is denoted by the “IS_SUCCESSFUL” which tells us if the money invested was used effectively.

```
<img width="1106" alt="Categorical_Variables" src="https://user-images.githubusercontent.com/111670866/213972115-810d358d-fd30-4da0-b347-413e54b866c2.png">

```
#### Features for the model 
The features include application type, affiliation, classification, use case, organization, status, income amt, special considerations, ask amt
```

```

#### Variables that are neither targets nor features
EIN and NAME are Identification columns and have been dropped for performing the analysis. 
```
<img width="930" alt="Dropped_columns" src="https://user-images.githubusercontent.com/111670866/213972144-0fbff820-3213-4d2a-ba86-eeff7f8d475b.png">

```
## Compiling, Training, and Evaluating the Model
#### How many neurons, layers, and activation functions did you select for your neural network model, and why?
I selected 2 hidden layers consisting of 80 and 30 neurons each. The First and second hidden layers ran the “Relu” activation function, whereas the output layer ran the “Sigmoid” activation function.

```
<img width="930" alt="Deep_Neural_Network" src="https://user-images.githubusercontent.com/111670866/213972243-1b055ecb-feb1-4c3f-8051-3e3dc7592063.png">

```
#### Were you able to achieve the target model performance?
This model didn’t achieve the target model performance. The result is as below:
```
<img width="930" alt="Checkpoint_Accuracy" src="https://user-images.githubusercontent.com/111670866/213972292-f618dd2a-635f-4605-b869-9fa068dde698.png">

```
 
#### What steps did you take to try and increase model performance?
To try and enhance the performance of the model I tried several things such as 
1)    Changing the activation function to sigmoid in the hidden layers and the output layers resulted in an accuracy of 65.46%
``` 
 <img width="930" alt="Activation_Accuracy" src="https://user-images.githubusercontent.com/111670866/213972379-8fb6f84e-50f7-48d8-b377-f1b642a6547e.png">

```
```
2)    Increasing the number of hidden layers to 3  resulted in an accuracy of 65.43%
```
 <img width="930" alt="Hidden_Layers_Accuracy" src="https://user-images.githubusercontent.com/111670866/213972397-6f41e2d9-144d-4ebe-8a9e-4506c12c0f26.png">

```
3)    Increasing the number of neurons in the hidden layers to 90 and 50 resulted in an accuracy of 65.42%
```
 <img width="930" alt="Increasing_Neurons" src="https://user-images.githubusercontent.com/111670866/213972410-f664ddb8-e399-4769-b29c-612efda3bf77.png">

```
# Summary:
 In all the above instances, the accuracy scores were similar at approximately 65%. However, this is a drastic reduction from the first attempt. The first attempt with 2 hidden layers, consisting of 80 neurons in the first hidden layer and 30 neurons in the second hidden layer and consisting of the ‘Relu’ activation function in the 1st and 2nd layers and the ‘sigmoid’ function in the output layer performed better with an accuracy of approximately 72.4%.
I would recommend using the Random Forest model instead of the deep neural model in this scenario.
While Deep Neural Networks (DNNs) are complex models and can be used for tasks such as image and speech recognition. Random Forest is an ensemble learning method that uses multiple decision trees to make predictions. DNNs are more computationally expensive and complex to train than Random Forest, but they can be more effective for certain tasks. Since Random Forest is relatively simple to train and interpret, and less prone to overfitting, it might be more suitable in this situation. 



