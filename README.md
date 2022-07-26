# airline-satisfaction
Udacity Data Scientist Nanodegree - Project I - Write a Data Science Blogpost

## Introduction
In this notebook, we aim to pinpoint reasons as to why airline passengers are so dissatisfied. We conduct exploratory analysis on the data, clean the data, and fit and test models against our training and testing data sets. Since the dataset is realtively balanced between our positive and negative results in the outcome class, minimal cleaning is required and balancing the data is deemed unnecessary. Here we are able to pinpoint specific factors that weigh on a customer's overall satisfaction or dissatisfaction - and can validate those variables and our intuitions through several handcoded models. The top three pipelines boast a 95% accuracy and ROC AUC score to validate that the variables we selected are among the most important features informing passenger satisfaction.

## Motivation
The reason I wanted to take on this dataset as opposed to some of the provided datasets is because I am enthusiastic about aviation and how data can improve and modernize the air travel industry - whether or operational or experiential. With passenger satisfaction becoming increasingly sour and airlines competing to imrpove their service and retain customers, I wanted to understand why exactly it is that customers are dissatisfied (or inversely, pleased with their travel experience). With this dataset I could do just that, and find out which factors prove the most important as to why customers are satisfied or not. Through this dataset I hope to better understand:
- Which service aspects most inform passenger satisfaction?
- Whether or not on-time performance plays as big a role in satisfaction as people make it seem?
- If its just coach flyers that are dissatisfied. Does service in a premium cabin make for a happier passenger?

## Libraries
For Exploratory Data Analysis - I utilized:
- Pandas (Version 1.2.4; Documentation - https://pandas.pydata.org/pandas-docs/version/1.2.4/)
- Numpy (Version 1.19.2; Documentation - https://numpy.org/doc/1.19/)
- Matplotlib (Version 3.3.4; Documentation - https://matplotlib.org/3.3.4/contents.html)
- Seaborn (Version 0.11.2; Documentation - https://seaborn.pydata.org/index.html)

For Model Assembly and Testing I utilized:
- Extreme Gradient Boosting (Version 1.3.3; Documentation - https://xgboost.readthedocs.io/en/release_1.3.0/contrib/release.html)
- Light Gradient Boosting Machine (Verseion 3.2.1; Documentation -https://lightgbm.readthedocs.io/en/v3.2.1/pythonapi/lightgbm.print_evaluation.html)
- Scikit Learn (Version 0.23.2; Documentation - https://scikit-learn.org/stable/whats_new/v0.23.html) 

## Environment and Other Utilities
As an apprentice for IBM, I wanted to gain more experience working in our cloud platform - [Cloud Pak for Data](https://www.ibm.com/products/cloud-pak-for-data?utm_content=SRCWW&p1=Search&p4=43700064659101157&p5=p&gclid=Cj0KCQjw_viWBhD8ARIsAH1mCd5GrPEqDW2wW9DETy_0TwncOBXuE1IwLUNjMZkLLuUpfqLiGwbUvFQaArJlEALw_wcB&gclsrc=aw.ds). The version of Cloud Pak for Data (CPD) that I used was CPD 4.0. I used CPD's Watson Studio to house the data assets and the Jupyter Notebooks in which I conducted my exploratory data analysis and modelling.

To compare and validate my intuitions and model results, I also ran the data through [Auto AI](https://www.ibm.com/cloud/watson-studio/autoai). Auto AI is a subset of IBM's Auto ML - which automates the machine learning process - including modeling, feature engineering, and pipeline comparison and selection. 

## File Descriptions
As far as the contents of this notebook - I used two data assets:
- **train.csv** : the training split of the original dataset, we will clean and encode this - and then fit it to our models.
- **test.csv** : the test split of the original dataset, which we will apply the same cleaning functions to in order to test our models.

## Summary of Results
Having cleaned and encoded the data to be ready to be ingested by our models, we also ran the data through a selector to get the fifteen most important features in regards to passenger satisfaction. We did this to make it easier for us and for our stakeholders to digest this information, and to reduce complexity and dimensionality of our model. These features are Travel Type, Flight Distance, Wi-Fi Service, Food and Drink, Online Boarding, Seat Comfort, On Board Service, Entertainment, Leg Room, Baggage Handling, Check-In, In Flight Service, Cleanliness, and Travel Class.

We then ran the training and test data splits through our models - and received favorable results. The most underperforming model still achieved an accuracy of 65% and an ROC AUC score of .64. The most optimal model - which achieved the best performance and performed the most efficiently (in consideration to both time and memory consumed) achieved an accuracy of 95.34% and a ROC AUC score of .95.

These models validate our intuitions in selecting these models as the most important considerations in determining customer satisfaction or dissatisfaction.

We then ran the training and test datasets through an optimized and automated machine learning platform to validate or correct our intuitions - which you can read about [here](https://medium.com/@chris.bacani7/why-are-airline-passengers-so-unhappy-73c8e25472ba)

## Acknowledgements
The dataset for this project comes from Kaggle.com (https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction)

Special thanks to [TJ Klein](https://www.kaggle.com/teejmahal20) for providing us with this dataset which has already been split into train and test portions and has a target column ready for modelling and testing. Additional thanks to [John D](https://www.kaggle.com/johndddddd) for acquiring the original [dataset](https://www.kaggle.com/datasets/johndddddd/customer-satisfaction).