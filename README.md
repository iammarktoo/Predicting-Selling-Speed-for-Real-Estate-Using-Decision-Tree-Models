# Predicting-Days-on-Market-for-Residential-Real-Estate-Sales-Using-Decision-Tree-Based-Models
This project explores the possibility of predicting the selling speed of residential properties in Brisbane using decision tree based models

# Project Structure
```bash
project/
│
├── property_data_analysis.ipynb # Main analysis notebook
├── Property_Data.xlsx
└── README.md
```
# Environment Setup
The project uses:

- Python (3.8+ recommended)
- Scikit-learn
- Pandas
- NumPy
- Matplotlib / Seaborn
- Jupyter Notebook
# Dataset Overview
The dataset contains 28509 records and 20 columns. The dataset includes residential property listings and attributes such as:

-	Location attributes: 
1.	Address (type: categorical)
2.	Suburb (type: categorical)
3.	State (type: categorical)
4.	Postcode (type: categorical)
-	Property attributes: 
1.	Number of beds (type: integer)
2.	Number of baths (type: integer)
3.	Number of parking (type: integer)
4.	Property size (type: float)
5.	Listed date (type: date)
6.	Listed price (type: float) 
7.	Sold date (type: date)
8.	Sold price (type: float)
9.	Property classification (type: categorical)
10.	Property sub classification (type: categorical)
-	Suburb attributes:
1.	Average days on market (type: integer)
2.	Average median price (type: float)

The target variable of the dataset is **days on market** (DOM), which is a **binary** variabe that was derived by comparing the actual amount of time a property has been on the market with their suburb's average. 

# Data Cleaning Steps
The notebook performs:

- Remove irrelevant attributes
- Adjust data types
- Handle missing values
- Remove outliers

# Exploratory Data Analysis
Performed visual and statistical inspections on:
- Relationship between property features and sold price
- Suburbs with the most sales
- Relationship between the average median sold price within a suburb and DOM
- Difference in the relationship between property size and DOM across different property types
- Correlation between all numeric attributes

# Machine Learning Models
Decision tree–based models used:
- Decision tree classifier
- Bootstrapped aggregation (Bagging) classifier
- Random forest classifier

Each model was evaluated using accuracy

# Model Hyperparameter Tuning
GridSearch was performed to determine the optimal combination of impurity score, model depth, minimum leaf sample size, as well as number of random features for random forest. 

# Model Evaluation and Findings
Key obsevations:
- Tree-based models were effective for capturing nonlinear relationships
- Bagging calssifier has the best performance among all of the tested decision tree based models

Full results are available in the notebook

