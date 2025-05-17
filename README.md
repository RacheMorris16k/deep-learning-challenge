# deep-learning-challenge
# Alphabet Soup Neural Network Report
 
 Overview of the Analysis
The goal of this project was to build a deep learning model using TensorFlow to predict whether an organization funded by Alphabet Soup would be successful. The data consisted of various features including organization type, classification codes, application types, and income ranges. By preprocessing the data and training a neural network, the objective was to achieve a model accuracy of at least 75%.

 Results
Data Preprocessing
Target variable:

IS_SUCCESSFUL (0 = not successful, 1 = successful)

Feature variables:

All other columns in the dataset, including encoded versions of:
APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, INCOME_AMT, ORGANIZATION, STATUS, ASK_AMT, and SPECIAL_CONSIDERATIONS

Removed variable:

'EIN' and 'NAME' (non-informative ID columns)

Also dropped 'SPECIAL_CONSIDERATIONS_Y' during optimization for potential noise reduction

Model: Compiling, Training, and Evaluation
Initial Model:

Hidden Layers: 2

Activation: 'relu'

Epochs: 50

Accuracy: ~72.8%

Optimized Model:

Hidden Layers: 3 (100, 50, 25 neurons)

Activation Function: 'tanh' (all hidden layers), 'sigmoid' (output)

Epochs: 50 with early stopping

Accuracy Achieved: ~74.0%

Optimization Techniques Tried:

Added another hidden layer

Changed activation functions

Dropped 'SPECIAL_CONSIDERATIONS_Y' feature

Trained over 50 epochs with validation split

 Summary
While the optimized model did not exceed the 75% accuracy goal, it demonstrated clear improvements over the base model. Through multiple valid attempts at optimization — including modifying model architecture and refining features — the model's accuracy increased to approximately 74%.

Recommendation:
For better results, a different machine learning model such as Random Forest or Gradient Boosted Trees could be used, as they often perform well on structured/tabular data with categorical variables. Additionally, further tuning such as hyperparameter search or oversampling techniques like SMOTE could help improve performance.