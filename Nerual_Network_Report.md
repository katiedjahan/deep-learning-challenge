# Neural Network Performance Report

## Overview
The purpose of this analysis is to be able to determine whether organizations will be successful if funded by Alphabet Soup. The model to make this prediction is built using data from previous organizations that Alphabet Soup has funded.


## Results
### Data Preprocessing
- The target for the model is the column “IS_SUCCESSFUL”, which has the data for whether or not the money was used effectively.
- The features for the model are:
![Alt text](<Images/Screenshot 2023-07-31 at 3.22.53 PM.png>)
- The columns “EIN” and “NAME” should be removed from the input data because they are neither targets nor features, just identification columns.

### Compiling, Training, and Evaluating the Model:
Neural Network Model Attempt 1:
- Hidden Layer 1: 20 neurons, `relu` activation
- Hidden Layer 2: 10 neurons, `relu` activation
- Output Layer: 1 neuron, `sigmoid` activation

Neural Network Model Attempt 2:
- Hidden Layer 1: 20 neurons, `sigmoid` activation
- Hidden Layer 2: 10 neurons, `sigmoid` activation
- Output Layer: 1 neurons, `sigmoid` activation

Neural Network Model Attempt 3:
- Hidden Layer 1: 20 neurons, `tanh` activation
- Hidden Layer 2: 10 neurons, `tanh` activation
- Output Layer: 1 neurons, `sigmoid` activation

In an attempt to increase model performance, I changed the number of neurons and the activation in the hidden layers, and to the preprocessing step I binned the "INCOME_AMT" column in addition to the "AAPLICATION_TYPE" and "CLASSIFICATION" columns. In the second attempt, I kept the preprocessing steps the same as the original model and changed the activation functions in the hidden layers from `relu` to `sigmoid`. I kept the number of neurons the same as the first attempt. In my third attempt, I changed the activation types in the hidden layers to `tanh`.
None of the three attempts achieved accuracy above 75%.


## Summary
None of the four models were able to achieve accuracy above 75%. The original model achieved accuracy of 0.7302623987197876. The highest accuracy achieved by any of the models was 0.7341107726097107 in the second optimization attempt. It appears that sigmoid is the best activation to use for this model, as other attempts with other activations had lower accuracy scores. Perhaps more neurons in the second optimization attempt would produce a higher accuracy score, but my machine was unable to accomodate for that.
### Original Model:
![Alt text](<Images/Screenshot 2023-07-31 at 4.16.12 PM.png>)
![Alt text](<Images/Screenshot 2023-07-31 at 4.17.06 PM.png>)
![Alt text](<Images/Screenshot 2023-07-31 at 4.17.43 PM.png>)

### Model Optimization Attempt 1:
![Alt text](<Images/Screenshot 2023-07-31 at 3.56.28 PM.png>)
![Alt text](<Images/Screenshot 2023-07-31 at 4.00.13 PM.png>)
![Alt text](<Images/Screenshot 2023-07-31 at 4.00.38 PM.png>)

### Model Optimization Attempt 2:
![Alt text](<Images/Screenshot 2023-07-31 at 4.01.22 PM.png>)
![Alt text](<Images/Screenshot 2023-07-31 at 4.01.39 PM.png>)
![Alt text](<Images/Screenshot 2023-07-31 at 4.02.08 PM.png>)

### Model Optimization Attempt 3:
![Alt text](<Images/Screenshot 2023-07-31 at 4.02.37 PM.png>)
![Alt text](<Images/Screenshot 2023-07-31 at 4.02.54 PM.png>)
![Alt text](<Images/Screenshot 2023-07-31 at 4.03.11 PM.png>)