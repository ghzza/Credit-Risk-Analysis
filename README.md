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
