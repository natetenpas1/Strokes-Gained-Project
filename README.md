# Strokes-Gained-Project
This is a machine learning project about professional golf analytics. I used two publicly available data sets  
  https://www.kaggle.com/datasets/jmpark746/pga-tour-data-2010-2018/data
  https://www.kaggle.com/datasets/jychoi87/pga-tour-top-200-player-data-20152019
to try and predict so-called "Strokes Gained" statistics, which are complicated to compute and involve large databases, from more conventional statistics that have existed for decades on the PGA TOUR. This is a natural analysis to undertake, and though I haven't seen it done, something of the like has been suggested in eg  
https://github.com/NishadKhudabux/Data-Science-in-Golf-Strokes-Gained-vs-Traditional-Metrics.
  
After cleaning and merging the data, I had roughly 700 player seasons to work with from 2015-2018. I performed Linear, Lasso, Ridge, and Support Vector (SVR) regressions (both kernel-based and linear), with hyper-parameter tuning and k-fold cross-validation. Every model which produced a linear regression function ultimately performed similarly. I settled on a linear SVR approach for my final model, which I then applied to my test data. The final model was better on some strokes gained areas than others, and I've listed each target variable with its final R^2 score.
* SG: Approach .74
* SG: Around the Green .43
* SG: Putting .66
* SG: Long .87

These R^2 variables, particularly the SG: Long figure, suggest we can do a pretty good job of using standard on-course statistics, along with a player's overall performance, to get a feel for whether their long or short game is driving their success (or lack thereof). 
I also included a basic primer on SVR, since it is less known than its cousin SVM (used for classification problems). Then, I did some analysis of what percentage of residuals fell within a desired threshold range, which is the kind of metric that SVR should specialize in. 
I have included my two jupyter notebooks, two CSV files with the data, and a longer writeup with my motivations, conclusions, existing work, and future work.

Skills: Python, numpy, pandas sklearn, data cleaning, merging data sets, regression problems, kernel methods, linear, lasso, ridge, support vector regression, matplotlib, k-fold cross validation, hyper-parameter tuning, sports analytics. 
