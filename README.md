# predictive-maintenance-ml
Predicting Remaining Useful Life (RUL) of turbofan engines with machine learning models (Random Forest, XGBoost, LSTM) for proactive maintenance and reduced downtime.
## overview
This project focuses on building a predictive maintenance system for turbofan engines using NASA’s CMAPSS dataset. The main aim is to estimate the Remaining Useful Life (RUL) of engines and predict failures before they actually happen. Doing this allows maintenance to be planned in advance, which reduces unexpected breakdowns, keeps schedules optimized, and improves overall reliability.

To tackle this, I experimented with different machine learning approaches — Random Forest, XGBoost, and LSTM — to see how they perform on both tabular and time-series data.
I tried out different approaches to see how well they perform:
 - **Random Forest** as a simple baseline model.
 - **XGBoost** to improve results on tabular data.
 - **LSTM** to handle the time-series nature of engine sensor data.


## Project Workflow
I built this project step by step as follows:

**Data Understanding & Cleaning**
Loaded the CMAPSS dataset, went through the sensor readings and operating settings, removed irrelevant/constant columns, and saved a cleaned version of the dataset.

**Feature Engineering & RUL Calculation**
Created Remaining Useful Life (RUL) labels for each engine and prepared the final set of features for modeling.

**Baseline Random Forest Model**
Trained a Random Forest regressor as a baseline, evaluated it using RMSE, MAE, and R², and also checked which features were most important.

**XGBoost & LSTM Models**
Used XGBoost for tabular predictions and LSTM for time-series sequence predictions. Compared their results and visualized how close predicted RUL values were to the actual ones.

**Model Evaluation & Comparison**
Collected metrics (RMSE, MAE, R2) for each model and compared their performance on predicting RUL.

**Visualizations**
Plotted actual vs predicted RUL, error distributions, and feature importance to better understand model behaviour.

**Saving Models & Processed Data**
Saved trained models (Random Forest, XGboost, LSTM) and intermediate datasets to they can be reused without retraining.

**Tech Stack** 
- Python
- Pandas, NumPy
- Scikit-learn
- TensorFlow / Keras
- XGBoost
- Matplotlib, Seaborn
- Google Colab  

*Dataset* 

I have used the NASA CMAPSS dataset for this project. It contains sensor readings, operational settings, and cycle information for multiple turbofan engines. Each engine runs until failure, which makes it suitable for predicting Remaining Useful Life (RUL).
*Models Methods*
For this project, I tried out different machine learning models to check which works better for RUL prediction. I started with Random Forest as a baseline, then moved to XGBoost for tabular data, and finally used LSTM to handle the time-series nature of engine cycles.

*Results*

I compared the models using RMSE, MAE, and R2 metrics.
 - **Random Forest** --> baseline performance.
 - **XGBoost** --> better accuracy on tabular features
 - **LSTM** --> captured sequence patterns and gave strong results.
let us look comparison of the above 3 models in the following table:
   **Model**          RMSE      MAE      R2
   Random Forest      34.17    24.39    0.72
   XGBoost            6.59     4.39     0.97
   LSTM               14.74    11.53    0.86

*Results visualization*

Here are some of the compppparison plots from the models:
**XGBoost - Actual vs Predicted RUL**
![XGBoost Results](results/actual_vs_pred_xgb.png)

**LSTM - Actual vs Predicted RUL**
![LSTM Results](results/actual_vs_pred_lstm.png)
*Future work*
I plan to improve this project by testing deep learning models( CNN-LSTM), and maybe deploying the best model as an API for real-time predictions.

*Acknowledgements*

Dataset is from NASA Prognostics Center of EXCELLENCE(CMAPSS).





   
