# Data Science Ephemeralization

The deluge of techniques in Data Science can can cause some ~~despair~~ dizzines. Nonetheless, **most** of the problems with face as practitioners of the craft boil down to some basic concepts and rules of thumb. Buckminster Fuller coined the term ephemeralization to describe the ability to do "more and more with less and less until eventually you can do everything with nothing". The *Data Science Ephemeralization* repo is a trial in devising a minimilistic mental framework for dealing with a wide range of problems.

![](ds-diagram.png)

Some basic cloud knowledge, version control, ssh, and a programming language will get you pretty far.

As a data scientist your three main responsabilities are:

- Define a feature engineering pipeline.
- Choose a useful model and evaluation metric.

I try to make this list minimal and comprehensive at the same time. Hope you can find something interesting over here. Some comments on tools, you will always 
use some kind of infraestructure to perform these activities. I am not a computer scientist myself, the two skill I found essential while performing the job where:

That said, The work done by the data scientist is **data-centric**. That means the data will dictate the path. Most of the time, you will work with 4 datatypes: 

- Tables
- Time series
- Images
- Text

Some notes on infraestructure.

## Feature engineering

The data comes from some process, the idea is to have the best possible data representation. 
The feature engineering process has a clear target: representing your data in a **numeric table without missing values**. That's it! Ok, I know, sometimes you just want
to preprocess your images and some models can deal with missing values. But those are the exceptions, not the rule. Other concept to keep in mind is 
[end-to-end learning](https://www.youtube.com/watch?v=ImUoubi_t7s). Some deep learning models are able to make good data representations themselves, killing two birs with
one stone: feature engineering and modeling.

### Table

The table is the most common data structure in data science. Even when you are working with the other data type you may have a data table at the end. 

- Missing values
- Outliers
- Categorical encoding
- Dimensionality reduction
    - Feature selection
    - Feature extraction

### Text

- Bag-of-words.
- Tf-idf.
- Embedding.

### Image



### Time

## Modeling

> "All model are wrong, but some are useful" - Box

Start with the easier part and stick with it. The evaluation metric is dictated by the type of problem you are dealing with:

- Classification
    - Binary classification
        - Recall
        - Precision
        - F1 Score
        - ROC Curve
        - AUC
    - Multilabel
- Regression
    - MAE
    - RMSE
- Clustering: harder.

Unless it's strictly necessary, **do not change your evaluation metric during the project**. Well, so far so good. The data guided my feature engineering process, the problem 
told me which metric I should use. What about the model? Bad news...

You only improve what you already do. Start with the basics and move from there.

Pandora's box. Link to knowledge-graph.

Import factors when choosing the model:

- Interpretation or acuracy?
- Computational resources:
    - Development:
    - Deployment:

### Assessing results and moving forward



[Evaluation and validation curves](https://scikit-learn.org/stable/modules/learning_curve.html)

Do you need more data?
Do you need more features?
Do you need a more flexible model?

## Resources

- feature engineering books
- Machine Learning Yearning.