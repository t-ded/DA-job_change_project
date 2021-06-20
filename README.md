# [Analysis of more than 19 thousand recruits for a Data Science company - Classification task - Project Overview:](https://t-ded.github.io/t-ded-portfolio/projects/project-2/)


## Project Summary

- Comprehensively **explored and visualized** the data, followed up by predicting the target variable with **accuracy of 0.73**.
- **Engineered thousands of missing values** based on the expected probability distribution of the feature.
- Implemented Classification Histogram Gradient Boosting, Linear Regression, and Random Forest algorithms, extracted **feature importance and performed feature selection**.
- My findings might have a **huge impact on the average time and money cost of new employees** if implemented correctly into the recruiting system of a company in DS field.
- In the future, the binary target variable may be switched for the continuous number of training hours, enabling me to try regression algorithms.
- Also, a **clustering analysis** may be performed onto the recruits, giving us even more precious insight into the fundamentals. This would also improve the data engineering.

## Project Background

- This dataset has been chosen as it revolves around a field I see my future in and the results may present a meaningful opportunity of application in practice
- The [initial dataset](https://www.kaggle.com/arashnic/hr-analytics-job-change-of-data-scientists?fbclid=IwAR2jKFzfv2xK7Uj8FQfnSHEicbpMFl0yAJHRLBRZfq98Xcy2dEz9W2bZAy8) consists of 19 158 reviews and 14 features, one of them being the dependent variable which tells us, whether or not the person is going to change their job and pursue career in the data science company. The test set then includes another 2 129 entries to be predicted.
- For this project, EDA, visualisation and data interpretation have been given priority over algorithms as it seemed to me that for this particular dataset, it would be much easier to actually implement the results in the form of graphs, charts and plots into business, rather than estimator predictions and their coefficients.

## Project Outline

- State the initial hypotheses
- Make necessary imports, take first look at the dataset, identify variables
- Engineer missing data in both continuous and categorical columns
- Univariate analysis
- Multivariate analysis (mainly in relation to training hours)
- Multivariate analysis in relation to target variable
- Correlation inspection
- Model set-up, skewness handling
- Model implementation

## Initial Hypotheses and Notes

- Trainees with more trained hours who do not enroll in the end are extremely costly 
  - Training hours is almost as important as the target variable
- City column in excessive since city development index holds much more information
- City development index may be positively correlated with target variable and relevant experience as Data Science is a rather modern field
- Gender may be correlated to target variable and relevant experience
  - Are genders equal in the field of data science?
- Relevant experience should have a huge impact on both training hours and target variable
  - Same might go for general experience
- People with STEM Major may be more likely to pursue career in the data science field
- People with higher education level are likely to require less training hours
- Training hours and target are unlikely to be very correlated
    
- Note: Among the features of the dataset are many variables whose analysis could be very interesting but
        would not be related to the purpose of this project (such examples include gender vs. enrolled university etc.)

## Hypotheses after examination

- City development does have positive correlation with relevant experience but is actually negatively correlated to the target variable
- Males are just a tiny bit more likely to have relevant experience and actually little less likely to become employees in the end
- People with relevant experience are way less likely to become employees in the end and require more training hours on average
- There is no clear relation between general experience and training hours, however, people with less experience are more likely to change the job
- The company is by far the most likely to succeed withing recruits with Graduate education level and least likely to employ a recruit with only Primary School
- Among people with Graduate education level, recruits with majors of Other, STEM and Business Degree are the ones to look for from the perspective of a company
- There is no significant impact of education on the number of training hours
- There is almost zero correlation between training hours and the target variable

## Possible next steps

- Automate the model creation/selection process
- Select the features much more carefully
- Pay more attention to model hyperparameters tuning
- Under some dubious assumptions and data from the internet we could add few features that the company did not collect
  - These would be for instance age, years of relevant experience
- Fill the missing data based on clustering algorithms rather than randomness and distributions
- Change the target variable to training hours and try to predict this value for each participant
  - A new value based on both of these columns could be created (one that would consider that recruits with most training hours who do not change their job are extra-costly)
