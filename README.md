# CNFs-MorFi2Mech
ML models for predicting CNFs mechanical properties from MorFi data.

This is a readme file for this paper:


####   A machine learning approach for the prediction of cellulose nanofibril films’ mechanical properties from suspension morphological data
Yasaman Asiaee1, Parinaz Rahimzadeh-Bajgiran2, Colleen Walker3, Douglas Bousfield4, Mehdi Tajvidi1 #####

1School of Forest Resources and Advanced Structures and Composites Center, University of Maine, 5755 Nutting Hall, Orono, ME 04469, USA
2School of Forest Resources, University of Maine, 5755 Nutting Hall, Orono, ME 04469, USA
3Process Development Center, University of Maine, 5737 Jenness Hall, Orono, ME 04469
4Chemical and Biomedical Engineering, University of Maine, 117 Jenness Hall, Orono, ME 04469

 The models predict the tensile strength and toughness of cellulose nanofibrils (CNFs) film using Linear Ridge Regression (LRR) and Random Forest (RF) based on MorFi data.

# Repository contents
The following Jupyter notebooks contain all necessary steps, including dataset import, data normalization, model training and testing on unseen data, prediction, 
feature importance analysis, and sensitivity analysis:

## Tensile strength prediction:

LRR_Final_model_tensile_strength.ipynb
RF_Final_model_tensile_strength.ipynb

##Toughness prediction:

LRR_Final_model_toughness.ipynb
RF_Final_model_toughness.ipynb


# To use the models on your own dataset, follow these steps:

1. Preprocess the Data
Use the Pre_processing script to format the raw MorFi data into a standardized dataset for the models.
2. Load and Run the Model
Load the trained model and apply it to your dataset using the following code:


import joblib
import pandas as pd

# Load the trained LRR model for tensile strength prediction (as an example)
loaded_model = joblib.load("LRR_tensile_strength.pkl")

# Load the test dataset (get from pre_processing code)
X_test = pd.read_csv("normalized_final_data.csv")

# Predict outcomes
y_pred = loaded_model.predict(X_test)

# Display predictions
print("Predicted Values:", y_pred)
















