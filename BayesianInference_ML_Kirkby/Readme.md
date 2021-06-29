# Intro to Machine Learning and Bayesian Inference

## Day 1

Slides are [here](https://docs.google.com/presentation/d/1IPAVxFkwyQwCEpC-KfvTOrnxoUKN2IxIK6NVmyXqM2U/edit?usp=sharing)

## Dataset Homework

Select a dataset to work with in tomorrow's session. It can be related to your research or hobbies or anything you are interested in.

The two main numbers  for any dataset are:
 - N = number of rows (samples): aim for N>100
 - D = number of columns (features): aim for D>10
 - keep N x D < 100,000 (trim rows or columns as necessary)

Any format that can be imported into pandas is ok. Pandas import functions have names like `read_csv` and are documented [here](https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html).

Kaggle is a good source of interesting open source datasets: https://www.kaggle.com/datasets

Once you have selected your data, check that you can import the following packages in a jupyter notebook:
```
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd
from sklearn import preprocessing, decomposition, ensemble, inspection
import seaborn as sns; sns.set()
```
Now check that you can read your data,  e.g.
```
df = pd.read_csv('mydata.csv')
```
Finally, add a description of your dataset to [this spreadsheet](https://docs.google.com/spreadsheets/d/1dhorqsz6x0zLBpXBQPWi0Z16raU4V60z1fAinApjIlU/edit?usp=sharing).

In case you do not have a dataset to work with, I have included three samples in this repo:
 - `covid.csv`: Vaccination rates and UN indicators for countries of the world (as of June 2021)
 - `fifa.csv`: Male soccer player statistics from FIFA'21 (Spain,Italy,France,Germany,England,Mexico 1st divisions only)
 - `titanic.csv`: Information about passengers on the Titantic

You can load one of these remotely, e.g.
```
df = pd.read_csv('https://raw.githubusercontent.com/cosmostatschool/MACSS2021/main/BayesianInference_ML_Kirkby/covid.csv')
```

## Day 2

Dataset preprocessing:
 - pandas [dropna](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.dropna.html): remove rows (samples) with invalid data
 - pandas [select_dtypes](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.select_dtypes.html): remove columns (features) with non-numeric values
 - sklearn [preprocessing.scale](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.scale.html): scale numeric features to have zero mean and std dev = 1

Estimate dataset dimensionality:
 - sklearn [decomposition.PCA](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html)
 - [Measure and reduce dimensionality](https://nbviewer.jupyter.org/github/dkirkby/MachineLearningStatistics/blob/master/notebooks/Dimensionality.ipynb) (notebook)

Estimate feature importance:
 - sklearn [random forests](https://scikit-learn.org/stable/modules/ensemble.html#forest)
 - sklearn [permutation importance](https://scikit-learn.org/stable/modules/permutation_importance.html)
 - [Case study: redshift inference](https://nbviewer.jupyter.org/github/dkirkby/MachineLearningStatistics/blob/master/notebooks/Redshift.ipynb) (notebook)
