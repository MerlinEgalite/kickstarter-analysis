# kickstarter-analysis

## Motivation

Finding money is one of the toughest challenges in the process of launching a project. Forinstance, a start-up is not always lucky enough to find business angels to invest in theproject. In the absence of such investors, there are two other ways to find money towardscitizens or companies.  First, a start-up can raise funds pledging to pay back investorswith interests: it is called crowd-lending. Otherwise, it can organize fundraising based ondonations: it is called crowdfunding. In both cases the main challenge is to give credit tothe start-up, and to persuade the investors by giving them guarantees of the probabilitiesof success of this project. Convincing the investors requires to offer every single elementthat ensure the future launching of the project. Thus, being able to give a probability ofsuccessfully reaching the amount of money needed is a very powerful argument on bothsides. For the investors, it brings guarantee and faith. They will be more willing to give orlend money to a start-up mathematically predicted to be successful. For the start-uppers,it becomes possible to maximize its probability of success, looking at all the componentstaken into account when computing this probability.  Indeed, visualization of the dataoffered by Kickstarter gives conclusions on the best features to have a successful project(date, name, category more likely to raise money).

How can we quantify the success of a start-up ? How can we predict the future of astart-up ? It is basically a classification problem given a set of projects: success or fail. Wewant to build a classifier, based on fitting a mathematical model to the data of Kickstarter,in which the two categories are « success » or «fail ». In other words, our project is aboutcreating a predictor based on the available data able to assess the chances of success ofany project. This data is made of past projects. Each project is described by intrinsiccharacteristics (country, date of launching, category of project) which form the inputs ofour model through detailed columns. Our goal is to collect this data, to pre-process it(« clean » data), to build various predictors (classification of the project in the categoryfuture success or future fail) such as Logistic Regression, Neural Networks, Random For-est, XG Boost, Grid Search, and finally to choose only one predictor based on precisioncriterion.

The final idea would be to create a web application on which investors could evaluatethe probability of success of a project and automatically transfer their money on the mostpromising projects based on our predictor.

Let us not forget that helping the emergence of promoting start-ups is a crucial socialchallenge because it also helps the development of innovative projects on several topicssuch as environment, health or technology. The predictor we want to build is made to helpboth investors and start-ups, so that the best projects will lead, at the end of the journey,to a concrete improvement of our societies. In the short term, our project seems to beabout money, but in the long term, our project is truly about society and innovation.

In conclusion, the predictor would answer a large part of the doubts of the investors.A positive prediction is a very strong argument in a negotiation. Indeed, guarantee for theinvestors means money for the start-up.

## Our repository

### Folder
- data: you will find the kickstarte datasets from https://webrobots.io/kickstarter-datasets/
- NNmodels: you will find the test models for Neural Networks classification
- zero_level_models: you will find our O level models loaded with pickle

### Code Files
- data_visualization: you will find data visualiation to a better understanding of the data
- general_preprocessing: you will find the code taken from Laura Lewis work on the subject: https://github.com/L-Lewis/Kickstarter-success-machine-learning
- lda, pca_58_components: you will find our tests to follow Laura Lewis recommendations that leads us to chose the log-transformation as the main method for preprcessing task
- neural_network: you will find our test to find a goos classifier with neural nets
- preprocessing_for_stacking: you will find the preprocessing tasks that allowed us to create the dataset on which we built our models for stacking
- log_grid_search: you will find the code which allowed us to find the best parameters for our 0 level models thanks to grid search algorithm
- create_model_for_stacking: you will find the code which allow us to build the 0 model for stacking
- stacking: you will find the code where we created our 1 level models and ran some test with grid_search
