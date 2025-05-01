Introduction

It is a revised report2 in "Comprehensive LSTM-based Cyber Attack Prediction" following the initial report of our research work.2. This research aims to build a predictive model using Long Short-Term Memory (LSTM) networks for cyber attack forecasting from historical host and network event data of Unified Host and Network Dataset (Kumar et al. 2020).

Upon receiving the first accepted proposal, the work has been conducted in the following steps: preprocessing of the data; development of a baseline model which acts as a bridge between inference and generation of more models. This latter is an attempt to answer the comments received during the first progress report.

Problem Definition

The cybersecurity field is continually threatened by strong attacks leveraging the underlying temporal patterns of the behavior of our systems. The conventional signature-based detection systems are usually unable to detect new threats or multistage attacks that change dynamically with advanced time (Wang et al. 2019). Such situations create a pressing need for predictive models working on sequence data of events to forecast breach's of opportunities.

Research problem The primary research problem is:

· Exposure of Time-Band behaviour in host and network event logs

· Building an LSTM model which surpasses the existing machine learning methods

Creating an AI model that could be put to work in cybersecurity operations

Significant challenges include, but not limited to: security log high dimensionality; class imbalance (e.g., attack events constitute < 15% in normal datasets); and interpretable model to security analyst (Moustafa and Slay 2019).
Methodology and Progress
Data Preprocessing
The following is done in dataset preprocessing phase.
Data cleaning: For numerical features, use interpolation to fill missing values, and for categorical variables, use mode imputation
Feature engineering: Developing temporal aggregates (rolling averages over 1-hour windows) of key metrics
Normalization: Use MinMax scaling for Numeric features (Range 0-1)
Generate sequences: wt sequence of fixed length (10-step) for LSTM input
Model Development
The following methods are implemented in the baseline LSTM architecture:
•	Two LSTM layers (with 128 units each), with dropout regularization of 0.3
•	Learning rate 0.001 Adam optimizer
•	Function loss binary cross-entropy
•	Batch size of 32 for training
Benchmarks have been performed with comparative models such as Random Forest (100 estimators) and SVM (RBF kernel)
Artefact Development
The current prototype includes:
Core Components
•	Data processing pipeline: Python scripts for automated data preparation
•	Training framework: Jupyter notebooks documenting model development
•	Visualization tools: Interactive dashboards showing attack trends
Conclusion
The project has made considerable progress since the first review, delivering all key milestones in the data preparation and baseline modeling stages. While the current results show that using LSTM based architectures for prediction of attacks is a feasible approach, they also reveal some scope for refinement. The project has maintained its development path and is on track to deliver the intended outcomes with optimised and deploy-ready models.
