# Results
*I added some of the answers, the old answer is still below. Feel free to edit my answer and Im open to any feedbakck -Rameez*

https://docs.google.com/document/d/1WqInJt89Ys7HtVmCQvcXF7ePTz2VBPu3pYU8hFIenoA/edit?usp=sharing

## Prediction Question and Overview

Our project investigates whether a country’s political and civil freedom can be predicted using its economic and demographic characteristics. Specifically, we ask: Can you predict the freedom of a country using its economic and demographic factors, and which factors have the greatest impact on the Freedom Index? 

## Key Results and Interpretation

Our key findings can be summarized in three insights. First, there is a strong positive correlation between economic prosperity and freedom: higher GDP per capita is consistently associated with higher freedom scores. Second, freedom varies considerably by region, with clear distinctions between high-freedom regions (Western democracies) and low-freedom regions (many countries in the Middle East and parts of Africa). Third, both PCA and Lasso confirmed that freedom is influenced by a wide array of variables. The lack of dramatic improvement from Lasso suggests that the predictors work together rather than individually dominating the outcome.

## Conclusion and Limitations

Economic and demographic variables do offer meaningful predictive power for national freedom, with GDP and Internet access being particularly useful indicators. However, the results also highlight the complexity of the phenomenon: freedom is not determined by a small set of features but instead emerges from a broader mix of socio-economic factors. Our model is limited by data quality, missing values, and the absence of institutional or historical variables that may play an essential role. It is also worth noting the potential for reverse causality—greater freedom may itself enable economic growth and education. While quantitative models like PCA and Lasso can offer valuable insights, a more comprehensive understanding of national freedom likely requires integrating qualitative political, historical, and institutional analyses.

### Old answer

**Clear prediction question**
Can you predict the freedom of a country using its economic and demographic factors, and which factors have the greatest impact on the freedom index?

  Our project consisted of performing principal component analysis and lasso on our data set. Initially the intent was to only perform principal component analysis on the data, but due to concerns with the coefficients we decided to perform lasso as well for a more representative model. 

  Within PCA we found that 18 components within the data were needed to explain 95% of the variance. 

  Ultimately lasso did not do a great job at explaining our data. Looking at the root mean squared error and R^2 these values are near equivalent to just using every column.

  List of  variables to drop:
  urban, rural split (leave in total)
  male, female split (leave in total)
 male, female unemployment (leave in total)
