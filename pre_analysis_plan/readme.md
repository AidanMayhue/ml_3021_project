# Pre-Analysis Plan

1. **Our Research Question** (1–2 paragraphs)  **(Done By Rameez)**
 * What are you trying to predict? Why is it interesting?  

- Does economic prosperity lead to more political and civil freedom
  
Rameez answer:
This study aims to investigate the relationship between economic prosperity and levels of political and civil freedom across countries. Specifically, we are looking to answer the question, Does economic prosperity lead to more political and civil freedom? This is a central question in international development, as many policymakers debate whether improving economic indicators (such as GDP growth, education, or internet access) correlate with or cause democratic reforms and greater civil liberties.

Understanding this relationship is crucial. If economic growth fosters freedom, then investing in development may lead to stronger institutions and better human rights. On the other hand, if no clear relationship exists or if prosperity can exist without freedom, it may challenge assumptions about global democratization. This question also has implications for foreign aid, international diplomacy, and long-term peacebuilding. Which are all topics that are prevalent today. 

2. **Observation Definition** (a couple sentences)  **(Done By Rameez)**
   * What is a single data point/ what does a row in our dataset represent in our study?
  
  Rameez answer:
  Each row in our dataset represents a country-year observation, combining political freedom scores and various economic indicators for a specific country in a specific year. In this study, a single data point reflects how politically free a country was in a given year and what its corresponding economic conditions were at that time. ​

3. **Our Prediction Type** (1 paragraph)  
   * Supervised vs. unsupervised? Classification or regression?
  
   We intend on using regression methods for our data, it would not make sense to track economic prosperity in terms of classification since the data in regards to economic prosperity is purely quantitative. We are using supervised learning methods as we already have the variables available and intend on using them to identify relationships between the variables.

4. **Planned Models and Methods** (2ish paragraphs)  
   * Which models are we going to use? Why? How will we tune or evaluate them?

  
Ian's Answer:
In our study, in order to investigate whether economic prosperity leads to greater political and civil freedom, we will use Principal Component Analysis (PCA) with the aim of reducing the dimensionality across our economic and demographic features. Our dataset utilizes a variety of features ranging from GDP growth rate and popluation distribution by age, to internet usage and and gross enrollment ratios. Due to these indicators being likely correlated, PCA will allow us to transform the features into smaller set of linearly independent principle components that we will use to capture as well as identify areas that are sensative in variance. This would reduce multicollinearity and return resulting variables that are more adequate for regression analysis. We will condunct PCA separately for the economic/demographic indicators and the freedom related scores to return interpretable summaries whcih will enable us to reflect how one predicts the other.

When we have the resulting principal components is computed, we will use multiple linear regression to model the relatinship between the predictors, which are economic principle components, and the targets, that being freedom principle components. We will use the resulting coefficient of determinatino (R^2) and cross-validation in order to asses the models generalizability as well as  explanatory power. We would also compare results to the original economic variables to confirm the PCA's effectiveness in reducing our feature dimensionality while also being able to preserve our predictive strength. Our modeling approach will allow us to test the association between economic prosperity and civil political freedom, allowing us to determine whether a country's economic features provide a adequate indication of it's freedom level.
     

5. **Success Metrics** (1 paragraph)  
   * How will we know that the the model is working? What metrics are we using?
  
     

6. **Anticipated Challengess** (1 paragraph)  
   * What are some potential challenges that we might face during the project
  
     

7. **Feature Engineering / Prep Work** (optional, 1 paragraph)  
   * How are we preparing the data before utilizing it for models and analysis
  
     

8. **Results Presentation Plan** (optional, 1 paragraph)  
   * How are we going to present the findings, graphs, charts, 

