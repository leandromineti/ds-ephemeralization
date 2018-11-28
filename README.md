# Data Science Ephemeralization

## TLDR

The solution lies in the problem:

- The data will tell you how to do feature engineering.
- The problem will tell you which metrics to use, choose one and stick with it.
- Nobody will tell you which model to use, build a basic one as fast as you can and move from there.

## Introduction

> "To think is to forget differences, generalize, make abstractions." - Borges

The deluge of techniques in Data Science can can cause some ~~despair~~ dizzines. Nonetheless, **most** of the problems with face as practitioners of the craft boil down to some basic concepts and rules of thumb. Buckminster Fuller coined the term ephemeralization to describe the ability to do *"more and more with less and less until eventually you can do everything with nothing"*. This repo is a trial in devising a minimilistic mental framework for dealing with a wide range of problems in Data Science.

![](ds-diagram.png)

As a data scientist, your job is choosing the paths along the above flowchart.

That said, The work done by the data scientist is **data-centric**. That means the data will dictate the path. Most of the time, you will work with 4 datatypes: 

- Tables
- Time series
- Images
- Text

I won't delve into the tools you will use to accomplish these tasks, but some basic cloud infraestructure knowledge, [version control](https://git-scm.com/), [ssh](https://en.wikipedia.org/wiki/Secure_Shell), and a [programming language](https://www.python.org/) will get you pretty far.

## Feature engineering

In order to best get the process being modeled, it is a hard problem. Highlighting informative relations. Removing noise. 

The data comes from some process, the idea is to have the best possible data representation.


The feature engineering process has a clear target: representing your data in a **numeric table without missing values**. That's it! But those are the exceptions, not the rule. Other concept to keep in mind is 
[end-to-end learning](https://www.youtube.com/watch?v=ImUoubi_t7s). Some deep learning models are able to make good data representations themselves, killing two birds with
one stone: feature engineering and modeling.

### Table

The table is the most common data structure in data science. Even when you are working with the other data type you may have a data table at the end.

- Missing values
- Outliers
- Categorical encoding
- Dimensionality reduction
    - Feature selection
        - Filter
        - Wrapper
        - Embedded
    - Feature extraction
        - PCA
        - t-SNE

### Text

- Bag-of-words.
- Tf-idf.
- Word embedding.

### Time series

Missing values

### Image

Not really transformed into a table nowadays. Some preprocessing and feeding it to a deep learning model.

## Modeling

> "All model are wrong, but some are useful." - George Box

You are not looking for the right model, you are looking for a useful one. Ok, let's begin at the end, before exploring the models define your metric. Almost certainly, your 
project will fall into one of three categories: classification; regression and clustering. Each one of them has its 

Start with the easier part and stick with it. The evaluation metric is dictated by the type of problem you are dealing with:

- **Classification**
    - Binary: recall; precision; F1-Score; AUC.
    - Multilabel: 
- **Regression**: MAE; RMSE; 
- **Clustering**: hard problem.

Unless it's strictly necessary, **do not change your evaluation metric during the project**. Well, so far so good. The data guided my feature engineering process, the problem 
told me which metric I should use. What about the model? Bad news...

You only improve what you already do. Start with the basics and move from there.

Choosing the right model for a phenomenom is like opening a [Pandora's box](https://leandromineti.github.io/ml-knowledge-graph/). We only improve what we already have. Start 
with a basic model you understand as fast as you can an move from there. While assessing many different models, and [combinations of them](https://mlwave.com/kaggle-ensembling-guide/), keep two concepts in mind:

- **Interpretation or acuracy?**
- **Computational resources**
    - Development: batch processing. Larger than memory. Spark. GPUs for deep learning, etc.
    - Deployment: the model will probably be deployed as an API and/or embedded in some form of ETL pipeline. Complex models tend to need a large amount of resources turning 
    the usage of the model technically or economically unfeasable.
- **Data**: mais pontos; mais features.
- **Model**: modelo mais flexível ou menos flexível.

### Assessing results and moving forward

[Evaluation and validation curves](https://scikit-learn.org/stable/modules/learning_curve.html)

## Resources

- feature engineering books
- Machine Learning Yearning.