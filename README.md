# deep-learning-challenge
 
# Deep Learning Model Analysis Report

## Overview

The purpose of this analysis was to develop and optimize a deep learning model to classify the success of charitable donations based on input features derived from the charity's attributes. This module challenge involves preprocessing data, selecting appropriate features, designing a neural network architecture, and iteratively improving the model to meet a target performance metric.

## Results

### Data Preprocessing

- **Target Variable(s):** The target for our model is `IS_SUCCESSFUL`, indicating whether the charity donation was used effectively.
- **Feature Variable(s):** The features for our model include all other variables except `EIN`, `NAME`, and `SPECIAL_CONSIDERATIONS`. These encompass various attributes of the charity organizations and donation details.
- **Variables Removed:** `EIN` and `NAME` were removed as they are identifiers not useful for prediction. Initially, `SPECIAL_CONSIDERATIONS` was also included but was later removed in an attempt to optimize the model.

### Compiling, Training, and Evaluating the Model

- **Neurons, Layers, and Activation Functions:** 
    - **V1 (Baseline Model):** Utilized two hidden layers with 80 and 30 neurons, respectively, and ReLU activation functions. The output layer used a sigmoid activation function for binary classification.
    - **V2 (Optimized Model):** Similar to V1 but removed the `SPECIAL_CONSIDERATIONS` column from the input data.
    - **V3 (Further Optimized Model):** Added a third hidden layer to improve prediction accuracy, keeping the activation functions the same.
    - 

- **Model Performance:**
    - **V1 Performance:** Loss: 0.5582, Accuracy: 72.76%
    - **V2 Performance:** Loss: 0.5567, Accuracy: 72.99% (After removing `SPECIAL_CONSIDERATIONS`)
    - **V3 Performance:** Loss: 0.5698, Accuracy: 72.93% (With an additional hidden layer)

- **Efforts to Increase Model Performance:** 
    - Removed features that were not contributing to the predictive power.
    - Experimented with the neural network architecture by adding more layers to capture more complex patterns.
    - Tried using other activation methods (did not improve performance).
    
## Summary

The deep learning models developed and iterated upon in this analysis achieved modest success in predicting the effective use of charity donations. The best-performing model (V2) achieved an accuracy of approximately 72.99%, a slight improvement over the baseline model. Adding an additional hidden layer in V3 did not significantly improve model performance and slightly increased the loss.

### Recommendation

For further improvement, maybe exploring other model architectures or machine learning algorithms might be beneficial. Also, changing the neuron/weight of each hidden layer might prove to be effective. Additionally, exploring more sophisticated neural network architectures, like those involving regularization techniques (L1/L2 regularization) or other activation functions, could potentially enhance model performance.Overall, eventhough an accuracy of 75% or higher was not achieved, potential improving next steps were identified. 

