# Intro to Machine Learning and Bayesian Inference

Day 1 slides are [here](https://docs.google.com/presentation/d/1IPAVxFkwyQwCEpC-KfvTOrnxoUKN2IxIK6NVmyXqM2U/edit?usp=sharing)

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
