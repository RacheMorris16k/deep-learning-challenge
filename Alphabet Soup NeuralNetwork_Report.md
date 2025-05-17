# Alphabet Soup Neural Network Report
## 1.Overview of the Analysis
The objective of this project was to build and optimize a deep learning model using TensorFlow to determine whether an Alphabet Soup-funded organization would be successful. The dataset contained categorical and numerical features related to each organization. The goal was to preprocess the data, design a neural network model, and optimize it for at least 75% accuracy.

## 2.Results
## Data Preprocessing

**Target Variable:**
IS_SUCCESSFUL: A binary column indicating if the organization was successful (1) or not (0).

**Feature Variables:**
All other columns after cleaning and encoding, including:

- 'APPLICATION_TYPE'
- 'AFFILIATION'
- 'CLASSIFICATION'
- 'USE_CASE'
- 'INCOME_AMT'
- 'ORGANIZATION'
- 'STATUS'
- 'ASK_AMT'
- 'SPECIAL_CONSIDERATIONS'

**Removed Variables:**

- 'EIN' and 'NAME' — IDs that don’t contribute to prediction
- 'SPECIAL_CONSIDERATIONS_Y' — dropped during optimization as it provided little variance

---

### Compiling, Training, and Evaluating the Model

**Model 1 – Base Model:**
- Hidden Layers: 2 layers (80, 30 neurons)
- Activation Functions: ReLU in hidden layers, Sigmoid in output
- Epochs: 50
- Performance: ~72.8% accuracy

##Model 2 – Optimized Model:##

- Hidden Layers: 3 layers (100, 50, 25 neurons)
- Activation Functions: Tanh in all hidden layers, Sigmoid in output
- Epochs: 50
- Adjustments:
Dropped SPECIAL_CONSIDERATIONS_Y

Added a third hidden layer

Changed activation function from 'relu' to 'tanh'

Performance: ~74.0% accuracy

## 3. Summary
While the optimized model did not surpass the 75% accuracy target, it showed improvement from the base model. Three valid optimization strategies were tested and applied.

Recommendation
A different classification algorithm such as a Random Forest or Gradient Boosting model might yield better results on this dataset, especially given its mix of encoded categorical and numerical features. Further tuning of batch size, learning rate, or dropout regularization could also improve deep learning performance.

--Rache Morris
--17/05/2025