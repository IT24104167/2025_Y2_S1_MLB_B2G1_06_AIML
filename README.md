# 2025_Y2_S1_MLB_B2G1_06_AIML
Data Pre-processing 

Project Overview

Objective

To build a robust AI model that can accurately classify whether a given system behaviour indicates the presence of ransomware or not. The goal is to support early detection and prevention of ransomware attacks using behavioural data.

Dataset Summary

The dataset contains system activity logs and behavioural features extracted from both benign and ransomware-infected environments. These features may include:

•	File system changes
•	Registry modifications
•	Process creation patterns
•	Network activity
•	Entropy and file access metrics
•	
Each record is labelled to indicate whether ransomware is present () or absent (), making this a supervised binary classification task.

Dataset details

Type	Tabular
Samples	62,000 samples
Features	16 variables

Target Label

Binary classification:
1 - Ransomware detected
0 - Benign activity

Format

CSV or Excel format
Cleaned and pre-processed
Group Members Roles

Member 1 - Detect and Removing Outliers 

IT24104206 
Nawarathna M.S.G

Check and report missing values (none here, but confirm).
Detect outliers in numerical features (e.g., DebugSize, ExportSize, ResourceSize).
Apply outlier treatment (IQR, log transform).
Confirm no duplicate entries.

Member 2 - Data Transformation 

IT24104192
Weerasooriya W.H.M.S.P

Handle scaling of skewed numerical features (DebugSize, ExportVA, etc.).
Apply standardization/normalization.
Ensure distributions are suitable for modelling.

Member 3 - Categorical Encoding 

IT24104198
Dahanayake D.Y

Drop irrelevant unique ID features (FileName, md5Hash).
Encode categorical features (e.g., Machine) using label encoding or one-hot encoding.
Ensure consistent encoding across training/testing sets.

Member 4 - Feature Engineering 

IT24104167
Jayawardena K.D

Create new binary flags (Has Debug, Has Export, Has Resources).
Derive ratios (ExportDensity, SectionDensity).
Drop irrelevant features with low predictive power.

Member 5 - Data Formatting

IT24104242
Panchali S.A.D.A

Validate data types (convert where necessary).
Ensure format consistency (numeric vs. categorical).
Standardize naming conventions (e.g., lowercase column names if needed).
Ensure no formatting inconsistencies.

Member 6 - Data Splitting & Balance

IT24104205
Harischandra M.A.W.V

Perform train/validation/test split (70/15/15).
Use stratified sampling on target (Benign).
Handle imbalances (SMOTE, under sampling, or class weights).
Provide the final prepared dataset to the group.


Noted - We shared the same Jupyter Notebook Files to preprocess the dataset and members parts are divided by comment from their IT number and name.
