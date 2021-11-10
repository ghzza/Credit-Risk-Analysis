# Credit-Risk-Analysis

## Project Description

This is a project to analyze a risk of customer credit data through clustering algorithm to cluster the data to good credit risk or bad credit risk and calculating total credit score through credit scorecard analysis. The chosen customer is the data which contain Good Credit Risk label and Accepted Label

## Objective

1. Visualize data and provide your thoughts with plots
2. Design Credit scoring engine
3. How to improve your model and approaches (Provide your thoughts and ideas)
4. How can we test model and deployment approaches (Provide your thoughts and ideas)


## Data Understanding

- Age (numeric)
- Sex (text: male, female)
- Job (numeric: 0 - unskilled and non-resident, 1 - unskilled and resident, 2 - skilled, 3 - highly skilled)
- Housing (text: own, rent, or free)
- Saving accounts (text - little, moderate, quite rich, rich)
- Checking account (numeric, in DM - Deutsch Mark)
- Credit amount (numeric, in DM)
- Duration (numeric, in month)
- Purpose (text: car, furniture/equipment, radio/TV, domestic appliances, repairs, education, business, vacation/others)

## Objective 1 - Visualize data and provide your thoughts with plots
### Notebook and Files :
1. Jupyter Notebook Files : Credit Risk Analysis_EDA (https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/Credit%20Risk%20Analysis_EDA.ipynb)
2. Raw Data : data_fs.csv (https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/data_fs.csv)
3. DataOri : DataForViz.csv (https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/DataForViz.csv)
4. ChosenCustomer Data : ChosenCustomer.csv (https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/ChosenCustomer.csv)
5. WorstCustomer Data : WorstCustomer.csv (https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/WorstCustomer.csv)
6. Tableau of Dashboard Visualization_DataOri : https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/Credit%20Analysis%20Visualization_DataOri.twb
7. Tableau of Dashboard Visualization_Chosen Customer : https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/Credit%20Analysis%20Visualization_ChosenCustomer.twb
8. Tableau of Dashboard Visualization_WorstCustomer : https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/Credit%20Analysis%20Visualization_WorstCustomer.twb

### Dashboard Visualization

For visualization dashboard please refer on this file image below : 
- Dashboard Visualization_DataOri : https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/Dashboard%20Visualization_DataOri.png
- Dashboard Visualization_Chosen Customer : https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/Dashboard%20Visualization_Chosen%20Customer.png
- Dashboard Visualization_WorstCustomer : https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/Dashboard%20Visualization_WorstCustomer.png

### Insight
#### Insight of Dashboard Visualization_DataOri : 
1. Most of Male Customer is 27 years old with 37 people in total and most of Female Customer is 23 years old with 32 people in total.
2. The most of customer for every purpose has little Saving accounts status, either they are Male or Female
3. The least of customer for every purpose has rich Saving accounts status, either they are Male or Female
4. The most of customer for every purpose has Skilled Job status, either they are Male or Female
5. The least of customer for every purpose has Unskilled - Non Resident Job status, either they are Male or Female
6. The most of customer who propose credit loan has Skilled Job status, Little Saving accounts status, and Own a house

#### Insight of Dashboard Visualization_ChosenCustomer :
##### Same insight compared to DataOri :

1. The most of chosen customer for every purpose has little Saving accounts status, either they are Male or Female
2. The least of chosen customer for every purpose has rich Saving accounts status, either they are Male or Female
3. The most of chosen customer for every purpose has Skilled Job status, either they are Male or Female
4. The least of chosen customer for every purpose has Unskilled - Non Resident Job status, either they are Male or Female
5. The most of chosen customer who propose credit loan has Skilled Job status, Little Saving accounts status, and Own a house

##### Difference insight compared to DataOri  : 

1. Most of Male Chosen Customer is 36 and 26 years old with 29 people in total who are 36 years old and 28 people in total who are 26 years old and most of Female Chosen Customer is 23 years old with 28 people in total.
2. The most purpose of customer in Chosen Customer is radio/TV

### Insight of Dashboard Visualization_WorstCustomer :
####Same insight compared to DataOri :

1. The most of worst customer for every purpose has little Saving accounts status, either they are Male or Female
2. The least of worst customer for every purpose has rich Saving accounts status, either they are Male or Female
3. The most purpose of customer in worst customer is Car

####Difference insight compared to DataOri  :

1. Most of Male Worst Customer is 29 years old with 4 people in total and most of Female Worst Customer is 24 years old with 3 people in total.
2. The most of worst customer for every purpose has Highly Skilled Job status, either they are Male or Female
3. The least of worst customer for every purpose has Unskilled - Resident Job status for Male and has Unskilled-Non Resident status for Female
4. The most of worst customer who propose credit loan has Highly Skilled Job status, Little Saving accounts status, and Own a house

### Correlation
#### Between features
1. Credit amount and Duration have moderately positive correlation between each other
2. The rest features have low positive/negative correlation between each other

#### Features to Target (cluster)
1. Credit amount has high negative correlation to the Target
2. Duration has moderate negative correlation to the Target
3. The rest features have low positive/negative correlation to the Target

## Objective 2 - Design Credit scoring engine
### Notebook and Files :
1. Jupyter Notebook Files : https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/Credit%20Risk%20Analysis_Clustering.ipynb
2. Input Dataset : DataForViz.csv (https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/DataForViz.csv)
3. Output Dataset : dfClustered (https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/dfClustered.csv)

### Clustering Method
- Features to be clustered : All Features
- Data : All data including outliers
- Algorithm : KMeans Clustering
- N-Clusters : 2 (Good Credit Risk and Bad Credit Risk)
- Visualization Features :
  - Dimensionality Reduction : PCA
  - Credit Amount VS Duration
  - Plot : Scatter Plots
- Evaluation Method and Score : 
  - Silhouette Score : 0.72
    - Best Cluster : 2
- Result :
  - the customers who have label "1" (Blue dot) is clustered as Good Credit Risk
  - the customers who have label "0" (Red dot) is clustered as Bad Credit Risk
  - Total data of Good Credit Risk is 827 data
  - Total data of Bad Credit Risk is 173

## Objective 3 - How to improve your model and approaches (Provide your thoughts and ideas)
### Method
I'm using Credit Scorecard analysis method to improve the model because it calculate total credit score of all data and evaluate all data to produce accepted or rejected label credits from the data

### Notebook and Files :
1. Main Jupyter Notebook Files : https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/Credit%20Risk%20Analysis_Credit%20Scorecard.ipynb
2. Support Files and Utilities : https://github.com/ghzza/Credit-Risk-Analysis/tree/main/Credit%20Risk%20Scorecard%20and%20Clustering/utilities
3. Input Dataset : dfClustered.csv (https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/dfClustered.csv)
4. Output Dataset :
   - Chosen Customer : ChosenCustomer.csv (https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/ChosenCustomer.csv)
   - Worst Customer : WorstCustomer.csv (https://github.com/ghzza/Credit-Risk-Analysis/blob/main/Credit%20Risk%20Scorecard%20and%20Clustering/WorstCustomer.csv)

### Credit Scorecard Step :
1. Load Data, Library, and Support Files & Utilities
2. Weight of Evidence (WoE) Analysis
3. Convert Training Data to WoE Values
4. Perform Classification Model to Predict Credit Score
5. Generate Credit Score for All Data, and Generate Score Table
6. Count Rejected and Accepted Customer
7. Slice the data to get The Chosen Customer
8. Slice the data to get The Worst Customer
9. Finish

### Next Step After Credit Scorecard Step : 
1. Create Supervised Multi-Output Classification Machine Learning Model to predict 2 targets of new data,Credit Risk Clusters and Accepted or Rejected Credit Score, automatically and all in inclusive.

### Reference for Credit Scorecard : 
1. https://towardsdatascience.com/how-to-develop-a-credit-risk-model-and-scorecard-91335fc01f03
2. https://towardsdatascience.com/intro-to-credit-scorecard-9afeaaa3725f
3. https://github.com/hurulee/scorecard

## Objective 4 - How can we test model and deployment approaches (Provide your thoughts and ideas)

### How to Test the Model
1. For clustering algorithm, which predict Good Credit Risk and Bad Credit Risk, is already tested through Silhouette Score evaluation method. And the result is the model able to separate the data and clusters perfectly

### Deployment Approaches
1. Create clustering model deployment from scratch with Flask or Cloud Services (GCP/AWS)
   - Reference step to deploy the model : https://towardsdatascience.com/how-to-build-deploy-an-unsupervised-learning-flask-app-from-scratch-afd3a18661a7
2. After the data already clustered, it can be processed manually to calculate total credit score through Credit Scorecard until we get Chosen Customer and Worst Customer data result.
3. Otherwise, we can create new machine learning model with Supervised Multi-Output Classification Model to predict 2 targets of new data,Credit Risk Clusters and Accepted or Rejected Credit Score, automatically and all in inclusive
4. Create Supervised Multi-Output Classification Model deployment from scratch with Flask or Cloud Services

  
