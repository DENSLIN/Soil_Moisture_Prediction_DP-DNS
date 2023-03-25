This is a machine learning model that predicts the soil moisture for given two datasets containing data about soil moisture, temperature and humidity.

# Project Team 
* Denslin Nunes - crce.9390.aids@gmail.com
* Nigel Misquitta - crce.9273.cs@gmail.com
* Dillon Gonsalves - crce.9259.cs@gmail.com
* Preeti Vasaikar - crce.9299.cs@gmail.com
* Shoydon Alphonso - crce.9240.cs@gmail.com






This repository consists of a single .ipynb file and a the provided datasets in .csv format.

# Working of this project

## Importing files
## Data Visualization
* Finding corelation between the features and soil moisture.
## Data Preprocessing 
* To extract Day, Month, Year, Hour and Minute(in intervals of 5 minutes) from 'ttime' into features on both datasets /*user1_data.csv*/ and /*user2_data.csv*/ .
* Plotting the scatterplots of all the features Vs soil moisture.
* Storing these new obtained datasets in /*data1.csv*/ and /*data2.csv*/ for further use.
## Combine Data
* Performing an outer join on /*data1.csv*/ and /*data2.csv*/ with common factors Day, Month, Year, Hour and Minute(in intervals of 5 minutes).
* The features obtained are as follows : Pm1_x, pm2_x, pm3_x, am_x, sm_x, st, lum_x, day, Month,year, hour, min, pm1_y,pm2_y, pm3_y, am_y, sm_y, lum_y, temp,humd,pres
* Now all the similar values from the above obtained features are averaged out.
* The resulting dataset obtained has features Pm1, pm2, pm3, am, sm, st, lum, day, Month,year, hour, min, temp,humd,pres.
* This dataset is stored in /*data_comb.csv*/ . 
## Model Data Preparation
* Dividing features(Pm1, pm2, pm3, am, st, lum, day, Month,year, hour, min, temp,humd,pres) and labels (sm).
## Model Testing
### Random Forest Regressor 
* RFR Imputation
* RFR An Extension to Imputation
### RFR Pipeline
* RFR pipeline Imputation
* RFR pipeline An Extension to Imputation
### XG Boost
* XG Boost Imputation
* XG Boost An Extension to Imputation

## Best Model
### RFR Pipeline An Extension to Imputation

* MAE: 31.739522397094426
* score: 0.9995207551616186
# Running the Model






## In order to get this project working we simply need to :



* Run the Soil_Moisture_Predicting_System.ipynb file in the repository.

* Make sure you run this file in either Google Colab (recmommended) or Jupyter notebook as it is a Jupyter source file.

* In Google Colab make sure you have uploaded all the datasets provided in this repository and also you enter the correct path to the datasets.

* In Jupyter Notebook make sure the path of all the respective datasets is entered correctly before running the program.

* **Run the following sections in the Soil_Moisture_Predicting_System.ipynb file :
--> Import 
--> Data Preprocessing
--> Combine Data
--> Model Preparation 
--> Best Model** 

    






# This repository consists of :

* Soil_Moisture_Predicting_System.ipynb file which is the main file consisting of the machine learning model built.

* user1_data.csv and user2_data.csv which are datasets that have been provided for training.
* data1.csv and data2.csv which are datasets obtained from the above two datasets after performing certain data preprocessing steps on the given datasets.

* data_comb.csv which is the final dataset obtained after merging data1.csv and data2.csv. This is the main dataset used for model training. 



* The  Soil_Moisture_Predicting_System.ipynb file also consists of a results section at the end of the file where we have compared all accuracy scores and Mean Absolute Error (MAE) of all the models that we have implemented. This helps us choose the best model for the prediction process.
