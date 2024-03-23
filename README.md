## End to End Machine Learning Project-

![Alt text](<Screenshot (5).png>)

1) Problem statement 
- This project understands how the student's performance (test scores) is affected by other variables such as Gender, Ethnicity, Parental level of education, Lunch and Test preparation course.


2) Data Collection
- Dataset Source - https://www.kaggle.com/datasets/spscientist/students-performance-in-exams?datasetId=74977
- The data consists of 8 column and 1000 rows.

#### Life cycle of Machine learning Project

- Understanding the Problem Statement
- Data Collection
- Exploratory data analysis
- Data Pre-Processing
- Model Training
- Choose best model

Exploratory Data Analysis (EDA): 
Through exploratory data analysis, 
 firstly i have checked for any missing and dublicate values by using df.isna().sum() and df.duplicated().sum() commands. Dataset does not cointain any missing and dublicate values.

Then i have gathered statistics of data set by using df.describe() -
From above description of numerical data, all means are very close to each other - between 66 and 68.05;
- All standard deviations are also close - between 14.6 and 15.19;
- While there is a minimum score  0 for math, for writing minimum is much higher = 10 and for reading myet higher = 17 

with the help of box plot we have detect the outliers 
sns.boxplot(df['math_score'],color='skyblue')

After that i have started exploring data
The starting step in exploring data was to define numerical & categorical columns
numeric_features = [feature for feature in df.columns if df[feature].dtype != 'O']
categorical_features = [feature for feature in df.columns if df[feature].dtype == 'O']

We have 3 numerical features and 5 categorical features

Now we have moved to data Visualization part
I created visualizations like histograms and scatter plots to understand the distribution of features and their relationships.

Some of the insight are
- Student's Performance is related with lunch, race, parental level education
- Females lead in pass percentage and also are top-scorers
- Student's Performance is not much related with test preparation course
- Finishing preparation course is benefitial.

. Model Selection and Training:

After evaluating different algorithms, I decided to use Linear Regression.I split the data into a training set and a testing set to train the model on historical data and evaluate its performance on unseen data."

"I evaluated the model using metrics like r2 score and
Accuracy of the model is 87.92
