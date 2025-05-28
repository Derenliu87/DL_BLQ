This is a machine learning strategy to quantify black-litterman's vector Q.
The prediction of vector Q in the black-litterman's model has always been a difficult point. How to measure it scientifically is very important.

Code features:
The strategy uses four machine learning algorithms, LSTM, Transformer, XGBoost, and Random Forest, to predict the closing prices of 10 ETFs and generate the opinion vector Q of the BL model.
Through empirical analysis, the performance of the BL model based on machine learning optimization is compared with traditional models (such as equal weight and risk parity models). The study selected 10 representative ETFs,used the AKShare API to obtain historical data, and improved the model training effect through feature engineering.

Quick Guide
1.The order of file code execution is as follows: data_acquisition, feature_engineering, model_training, bl_model, portfolio_optimization, performance_evaluation and main file.
2.data_acquisition is responsible for executing: reading target data, data characteristics, time length, technical indicators, etc. (can be modified according to needs)
3.feature_engineering is responsible for executing: screening engineering features for technical indicators, four machine learnings independently perform multicollinearity processing on each feature, calculate the correlation matrix between indicators, and remove features with correlation greater than 0.8. Random forest regression is then used to sort features by importance, and finally an actinic cross-check is performed to obtain the number of features and feature subsets with the largest scores (which can be modified as needed)
4.Model_training is based on four machine learning trainings and generates prediction results as vector Q (the model can be independently tuned as needed)
5.bl_model will read the vector Q calculated by the four models (the corresponding parameters in BL can be adjusted)
6.portfolio_optimization obtains the results based on four machine learning trainings and compares them with the results of the equal-weight and risk parity models.
7.performance_evaluation is responsible for generating visual charts
8.The main file is responsible for directly calling all files for calculation

Get Help
You can contact the author via email: derensunan@gmail.com (please state your purpose)
