# Salary Prediction

This project is building a salary prediction model based on various parts of a job description. The original data set contained variables such as Job ID, Company ID, Job Type, Degree, Major, Industry, Years of Experience, and Miles from Metropolis.

## About the Data

The data included numeric and categorical variables. There were no null elements within the data set, however there were five job IDs which reported zero salary. They zero salary roles shared no attributes or distinguishing elements to indicate that the zero salary was a real data point, so I chose to remove these job IDs as it seemed like harmlessly missing data. This left me with 999,995 observations.

## Data Cleaning & Exploration

Looking through the data to find key insights that may help me with my predictive analysis, I wanted to take a look at data that was not missing but potentially incorrect. I saw that less than 6% of jobs had a higher level of education with no major listed; given the low number of observations where I would have major missing, I chose to preserve the observations I had and leave the no majors in the total data frame. Nothing seemed to tie these jobs together.

I noted that the distribution of the salary data was slightly right skewed.

While there was no difference in degree type count by industry, Janitors are entirely made up by high school graduates and individuals who have not completed their education. Degree type was evenly represented amongst the other positions.

There appeared to be a slightly positive correlation between Job Type and Degree with salary. This influenced me to choose ordinal numeric class transformation for these two variables to ensure that I was capturing the slightly ordinal nature when assigning the values numerics for modeling.

Unlike Job and Degree Type, Industry didn't indicate any discernible order or ranking. I chose to dummy out these values individually to evaluate their correlation to salary (example, ENGINEERING would become its own feature with a 0 for jobs that were not in the field and a 1 for jobs that were in the field).

After these transformations, I took a look at the correlations of each feature with salary to determine which features to include in my modeling efforts. I set a threshold of -0.09 to 0.09 on which features to include.



## Baseline & Hypothesis


## Model Development
