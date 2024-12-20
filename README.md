# RapidUseML

Minimalistic Machine Learning Toolset used for quick training and usage of various models. 
One click for training, one click for prediction.


## Usage:

### Basics:

Prepare basic necessities for usage.

```
import RapidUse                                            # Ensure class is imported.
ml = RapidUse.ML()                                         # Create instance of class.
from pandas import read_csv                                # Get pandas to read CSVs.
```


### Prediction:

Predicts target value(s) based on input data provided, with automated model identification.
Note: ML.prdict(...) checks the folder and all directories within the folder its located in for the relevant model. 

```
#Load dataset for pred.
input_dataset = read_csv("input_dataset.csv")              

# Prediction target.
target_column = "column_d"                                   

# Try to obtain ML pred.
prediction_set = ml.predict(input_dataset, target_column)  
```

### Training:

Trains many models based on dataset, select top 3 and optimise them for better performance.

```
# Load dataset for training.
training_dataset = read_csv("training_dataset.csv")

# What features to predict with.
input_column_names = ["column_a", "column_b", "column_c"]         

# What component you want predicted.
target_column = "column_d"              

# What data % to dedicate to training.
train_test_ratio = 0.8                                     
ml.train(training_dataset, input_column_names, target_column, train_test_ratio)
```
