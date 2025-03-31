# Pre-Analysis Plan

1. **Our Research Question** (1–2 paragraphs)  **(Done By Rameez)**
 * What are you trying to predict? Why is it interesting?  

- Does economic prosperity lead to more political and civil freedom

  This study aims to investigate the relationship between economic prosperity and levels of political and civil freedom across countries. Specifically, we are looking to answer the question, Does economic prosperity lead to more political and civil freedom? This is a central question in international development, as many policymakers debate whether improving economic indicators (such as GDP growth, education, or internet access) correlate with or cause democratic reforms and greater civil liberties.

  Understanding this relationship is crucial. If economic growth fosters freedom, then investing in development may lead to stronger institutions and better human rights. On the other hand, if no clear relationship exists or if prosperity can exist without freedom, it may challenge assumptions about global democratization. This question also has implications for foreign aid, international diplomacy, and long-term peacebuilding. Which are all topics that are prevalent today. 

2. **Observation Definition** (a couple sentences)  **(Done By Rameez)**
   * What is a single data point, What does a row in our dataset represent in our study?
  
  Each row in our dataset represents a country-year observation, combining political freedom scores and various economic indicators for a specific country in a specific year. In this study, a single data point reflects how politically free a country was in a given year and what its corresponding economic conditions were at that time. ​

3. **Our Prediction Type** (1 paragraph) **(Done By Aidan)**
   * Supervised vs. unsupervised? Classification or regression?

   We intend on using multiple linear regression to predict the total freedom score of countries, based on their economic and demographic factors. While the available data makes it possible to do a classification model, we have opted to do regression instead, as this will return predictions that differentiate each country, even those within the same categorical label of freedom. Since, the data contains the target variable (total freedom score) necessary for supervised learning, and a multitude of independent variables, we have decided that multiple linear regression is the best method to answer our research question.

4. **Feature Engineering / Prep Work** (optional, 1 paragraph) **(Done By Brian)** 
   * How are we preparing the data before utilizing it for models and analysis?
  
  Beyond cleaning the data, which was done in the EDA process, some feature engineering is necessary for the model. There is a significant amount of missing data, spanning across most variables in the data. To address this, missing values will be imputed using the country’s mean on the missing variable across all years the country appears. If the value is missing for every year the country appears in the data set, the regional mean will be used instead. In the case that neither of these options work, the row will have to be dropped. Due to the moderate to strong correlation between many economic and demographic variables, principal component analysis will be used to reduce the effects of multicollinearity, and lower the dimensionality of the feature space into a collection of uncorrelated principal components. Before the principal component analysis, however, the features will be standardized to account for the sensitivity of PCA to scale.

5. **Planned Models and Methods** (2ish paragraphs) **(Done By Ian)**
   * Which models are we going to use? Why? How will we tune or evaluate them?

  In our study, in order to investigate whether economic prosperity leads to greater political and civil freedom, we will use Principal Component Analysis (PCA) with the aim of reducing the dimensionality across our economic and demographic features. Our dataset utilizes a variety of features ranging from GDP growth rate and population distribution by age, to internet usage and gross enrollment ratios. Due to these indicators being likely correlated, PCA will allow us to transform the features into smaller set of linearly independent principle components that we will use to capture as well as identify areas that are sensative in variance. The number of principle components used will equal the number of components necessary to reach a cumulative explained variance of 95%. This would reduce multicollinearity and return resulting variables that are more adequate for regression analysis. We will condunct PCA separately for the economic/demographic indicators and the freedom related scores to return interpretable summaries whcih will enable us to reflect how one predicts the other.

  When we have the resulting principal components is computed, we will use multiple linear regression to model the relatinship between the predictors (economic principle components), and the target (total freedom score). We will use the resulting coefficient of determinatino ($R^2$) and cross-validation in order to asses the models generalizability as well as  explanatory power. We would also compare results of the multiple linear regression using the principle components to the MLR using the original economic variables to confirm the PCA's effectiveness in reducing our feature dimensionality while also being able to preserve our predictive strength. Our modeling approach will allow us to test the association between economic prosperity and civil political freedom, allowing us to determine whether a country's economic features provide a adequate indication of it's freedom level.
     
6. **Success Metrics** (1 paragraph) **(Done By Brian)**
   * How will we know that the the model is working? What metrics are we using?
  
  Whether or not the approach/model “works” will be based on the $R^2$ coefficent of determination of the multiple linear regression on the test data, as well as the root mean squared error of the predicted freedom score values. The $R^2$ value will be used to determine the extent to which the freedom score of a country can be explained by its economic and demographic factors. The RMSE will be used to measure how far off the freedom scores predicted by the MLR are from the actual freedom scores. If the model is successful, we would expect to see an $R^2$ value greater than 0.5, along with an RMSE in or below the range of 10-15. The degree of success of the model would vary for $R^2$ and RMSE values outside of these ranges, with lower $R^2$ values and higher RMSE values indicating a worse/less sucessful model. 
     
7. **Anticipated Challenges/Weaknessess** (2 paragraphs) **(Done By Aidan and Claire)** 
   * What are some potential challenges/weaknesses that we might face during the project? How will we deal with them if they come up? If our approach fails, what will learn from this outcome? 

  I think a significant challenge we face in the data is deciding how many principle components to use. Too few principle components would capture too little of the explained variance, while too many would make the PCA process effectively pointless. We will address this by using as many principle components as necessary to account for 95% of the explained variance. PCA is most effective when the columns of data are highly correlated with each other. If many of these columns are independent, we would expect to see a less effective model as a result. If our data contains too many very uncorrelated columns (which we do not believe to be the case), doing principle component analysis will harm the performance of the MLR model, rather than help it. As a result, we will also perform MLR on the original features, not just the principle components, and compare the results of the two strategies. 
  
  Another potential weakness we may face is seperating factors of correlation. Predicting correlation between variables or ensuring that outside variables are not effecting the data would weaken our data. It's best to approach these situations with nuance, looking deeper in to the way these variables may affect eachother, and exploring unexpected correlations. If variables outside of our data set are better predictors of total freedom score than those in it, it would likely mean our approach would fail, due to a lack of predicitve power of the features in the data. If our approach fails, we would learn that the relationship between economic prosperity and political/civil freedom either can’t be understood using the features in our data, or can’t be understood using multiple linear regression, and may require a more complex model which takes into account non-linear relationships in order to answer our research question.


8. **Results Presentation Plan** (optional, 1 paragraph) **(Done By Kalenga)**
   * How are we going to present the findings?

   The findings will be presented using graphs and tables, emphasizing the process and results of using PCA and MLR to determine the relationship between economic prosperity and political/civil freedom. We will present the process of determining the number of principle components through a scatterplot to show how the cumulative explained variance increases with the number of components, and what number of components puts the explained variance passed the 95% threshold. Additionally, a table of regression coefficients for the PCA and non-PCA multiple linear regression will be presented, along with their $R^2$ values and root mean squared error for model evaluation.

     
  
  

