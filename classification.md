
 •	Supervised Learning
 This data has LABEL 

We should use classification for that and use something like KNN

* For some data we use scaling for prediction because the diffrence between data is high.
* For data we use standardization 
       (X – μ) / σ
      where X is a normal random variable, μ is the mean of X, and σ is the standard deviation of X.
* Class imbalance in classification problems arises when the number of observations belonging to one class is lower than the other
      Ensemble learning combines multiple models to obtain a robust model and has been prominently used with data augmentation methods to address class imbalance problems.
* Missing data is so important

import pandas as ps
cancer = pd.read_csv('...')
cancer['column'].unique()
cancer.info()

for rename : 
cancer["diagnosis"] = cancer["diagnosis"].replace({
    "M" : "Malignant",
    "B" : "Benign"
})

for calculate percentage : 100 * cancer.groupby("diagnosis").size() / cancer.shape[0]

cancer["diagnosis"].value_counts()

cancer["diagnosis"].value_counts(normalize=True)


![image](https://github.com/user-attachments/assets/c107d720-6c73-4acf-a9e9-5f6ec31d7316)
