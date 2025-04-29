**Results**

**Clear prediction question**
Can you predict the freedom of a country using its economic and demographic factors, addiitonally predicting which factors have the highest impact on the freedom index.

  Our project consisted of performing principal component analysis and lasso on our data set. Initially the intent was to only perform principal component analysis on the data, but due to concerns with the coefficients we decided to perform lasso as well for a more representative model. 

  Within PCA we found that 18 components within the data were needed to explain 95% of the variance. 

  Ultimately lasso did not do a great job at explaining our data. Looking at the root mean squared error and R^2 these values are near equivalent to just using every column.

  List of  variables to drop:
  urban, rural split (leave in total)
  male, female split (leave in total)
 male, female unemployment (leave in total)
