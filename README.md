# Neural_Network_Charity_Analysis

## Project Overview
A non-profit foundation would like a binary classifier that is capable of predicting whether applicants will be successful if funded by them. This project will utilize neural networks using the TensorFlow platform in Python. 

They would like to see the following:
  - The processing of the dataset provided for the neural network model
  - Compilation, training and evaluation of the model
  - Optimization of the model

## Resources
- Data Source: charity_data.csv
- Software: Jupyter Notebook 6.4.5

## Results

### Data Preprocessing
  - Original data is transformed by dropping the **EIN** and **NAME** columns
  - Target variable for the model is **IS_SUCCESSFUL**
  - Feature variables are **APPLICATION_TYPE**, **AFFILIATION**, **CLASSIFICATION**, **USE_CASE**, **ORGANIZATION**, **INCOME_AMT**, "**SPECIAL_CONSIDERATIONS**
  - Categorical variables are transformed by encoding

### Compiling, Training, and Evaluating the Model
#### Neural Network Model Breakdown
![alt text](https://github.com/thehatch4815162342/Neural_Network_Charity_Analysis/blob/main/images/model.png) 
  - Two Hidden Layers
    - Layer 1 has 80 neurons
    - Layer 2 has 3 neurons
    - Both layers use ReLU 
  - Output layer uses Sigmoid

#### Neural Network Model Results
![alt text](https://github.com/thehatch4815162342/Neural_Network_Charity_Analysis/blob/main/images/model_results.png) 

### Model Optimization
The goal is to opitimize the model in order to achieve a target predictive accuracy higher than 75%.

#### First Attempt - Change Activation Function
  - Both hidden layers activation function are changed from ReLU to Tanh
![alt text](https://github.com/thehatch4815162342/Neural_Network_Charity_Analysis/blob/main/images/first_attempt.png) 

#### First Attempt - Results
![alt text](https://github.com/thehatch4815162342/Neural_Network_Charity_Analysis/blob/main/images/first_attempt_results.png) 

#### Second Attempt - Change Activation Function, Double Neurons
  - Both hidden layers activation function are changed from ReLU to Tanh
  - Both hidden layers neurons have doubled so layer 1 now has 160 and layer 2 has 6
![alt text](https://github.com/thehatch4815162342/Neural_Network_Charity_Analysis/blob/main/images/second_attempt.png) 

#### Second Attempt - Results
![alt text](https://github.com/thehatch4815162342/Neural_Network_Charity_Analysis/blob/main/images/second_attempt_results.png) 

#### Third Attempt - Change Activation Function, Decrease Neurons by 20, Add Layer
  - Both hidden layers activation function are changed from ReLU to Tanh
  - A third hidden layer is added, activation function is set to ReLU
  - Hidden layers neurons decrease by 20 starting with layer 1 at 60
![alt text](https://github.com/thehatch4815162342/Neural_Network_Charity_Analysis/blob/main/images/third_attempt.png) 

#### Third Attempt - Results
![alt text](https://github.com/thehatch4815162342/Neural_Network_Charity_Analysis/blob/main/images/third_attempt_results.png) 

## Summary
The third attempt at optimization had the best results with a 73.03% accuracy, however, this was not the ideal goal. Since this is a binary classification problem, using Logistic Regression model could produce a better outcome. Neural networks are more difficult to train and are more prone to overfitting than logistic regression.
