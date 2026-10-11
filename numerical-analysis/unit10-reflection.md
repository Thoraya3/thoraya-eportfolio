# Numerical Analysis – Unit 10 Reflection

<br>

## What? (Description)

In Unit 10 of Numerical Analysis, I studied correlation and regression analysis and explored how relationships between variables can be measured, interpreted, and used for prediction. The unit focused on understanding correlation coefficients, scatter plots, simple linear regression, and multiple regression models.

<br>

The lecture materials introduced correlation as a statistical measure that describes the relationship between two variables. I learned that correlation measures both the strength and direction of a relationship. The unit explained the difference between independent and dependent variables and demonstrated how relationships can be visualised using scatter plots.

<br>

I learned that Pearson’s correlation coefficient, represented by r, ranges from -1 to +1.

<br>

- r = +1 indicates a perfect positive correlation.
- r = -1 indicates a perfect negative correlation.
- r = 0 indicates no linear relationship.

<br>

The unit also introduced regression analysis. Unlike correlation, which measures association, regression provides a framework for modelling and predicting the relationship between variables.

<br>

As part of the practical work, I completed Data Activity 8 using the Health_Data dataset, which involved investigating the relationship between systolic and diastolic blood pressure and producing a scatter plot.

<br>

The Unit 10 seminar focused on Correlation and Regression and explored the interpretation of correlation coefficients, scatter plots, regression equations, residuals, R² values, and hypothesis testing within regression analysis.

<br>

---

<br>

## So What? (Interpretation)

Unit 10 significantly improved my understanding of the difference between correlation and regression. Before studying this topic, both methods appeared similar because they examine relationships between variables. However, I learned that they serve different purposes.

<br>

Correlation measures the strength and direction of an association between two variables. Importantly, correlation does not imply causation. Two variables can have a strong correlation without one causing the other.

<br>

The seminar reinforced this distinction by explaining that correlation is symmetrical. Correlation between variable A and variable B is identical to correlation between variable B and variable A. Regression analysis is different because it introduces direction and attempts to explain how changes in one variable affect another.

<br>

I also learned that scatter plots provide an important visual assessment of whether a linear relationship appears to exist before statistical tests are performed. Scatter plots can reveal trends, clusters, outliers, and patterns that may not be obvious from numerical outputs alone.

<br>

Another valuable concept was the interpretation of R². The coefficient of determination measures the proportion of variation in the dependent variable explained by the regression model. For example, an R² value of 0.85 indicates that approximately 85% of the variation in the outcome variable is explained by the model.

<br>

As a Senior Application Programmer in the telecommunications industry, these concepts are directly applicable to my work. Correlation analysis could be used to investigate relationships between system performance metrics, network events, application response times, automation execution times, service requests, or incident volumes. Regression analysis can then be used to model trends and predict future outcomes.

<br>

The seminar also highlighted the importance of hypothesis testing when moving from sample-based observations to population-level conclusions. Statistical significance testing helps determine whether observed relationships are likely to exist beyond the sample used in the analysis.

<br>

---

<br>

## What Next? (Action)

Going forward, I plan to continue developing my ability to use correlation and regression techniques within R and other analytical tools.

<br>

I will focus on:

- Producing and interpreting scatter plots.
- Calculating Pearson correlation coefficients.
- Using Spearman and Kendall correlations when appropriate.
- Building simple linear regression models.
- Understanding residual analysis.
- Interpreting regression coefficients.
- Evaluating R² and Adjusted R² values.
- Testing model significance using p-values and F-statistics.

<br>

Within my professional role, I intend to apply these methods when examining relationships between operational metrics, automation performance indicators, service-management data, and application-performance measurements.

<br>

I will also continue documenting code, statistical outputs, visualisations, and reflections within my GitHub e-portfolio as evidence of my learning journey and preparation for future assignments and research work.

<br>

---

<br>

## Data Activity 8 – Correlation Analysis Using Health_Data

<br>

Data Activity 8 required the use of the Health_Data dataset to perform correlation analysis and visualisation.

<br>

### Task 1: Correlation between Systolic and Diastolic Blood Pressure

<br>

The objective of the first task was to calculate the correlation between systolic blood pressure and diastolic blood pressure.

<br>

Example R code:

```r
cor(
  Health_Data$sbp,
  Health_Data$dbp,
  use = "complete.obs"
)
```

<br>

This activity demonstrated how Pearson’s correlation coefficient can be used to measure the strength and direction of a relationship between two numerical variables.

<br>

### Task 2: Scatter Plot

<br>

The second task involved producing a scatter plot showing the relationship between systolic blood pressure and diastolic blood pressure.

<br>

Example R code:

```r
plot(
  Health_Data$sbp,
  Health_Data$dbp,
  main = "Scatter Plot of Systolic and Diastolic Blood Pressure",
  xlab = "Systolic Blood Pressure",
  ylab = "Diastolic Blood Pressure"
)
```

<br>

The scatter plot provided a visual representation of the relationship and supported interpretation of the correlation coefficient.

<br>

### Learning from Data Activity 8

<br>

Through this activity, I improved my ability to:

- Calculate correlation coefficients.
- Interpret the strength and direction of relationships.
- Create and interpret scatter plots.
- Identify patterns within data.
- Apply statistical analysis in R.

<br>

---

<br>

## Unit 10 Seminar – Correlation and Regression

<br>

The Unit 10 seminar extended the lecture content by focusing on practical interpretation and application of correlation and regression analysis.

<br>

### Seminar Questions

<br>

The seminar explored the following questions:

1. What is correlation analysis and what does r = 0 indicate?
2. What is the range of Pearson’s correlation coefficient?
3. When should Spearman’s or Kendall’s correlation be used?
4. What is the purpose of a scatter plot?
5. What does the intercept (β₀) represent?
6. What is the purpose of residuals?
7. What does an R² value of 0.85 indicate?

<br>

### Key Learning Points

<br>

The seminar reinforced that:

- Correlation measures association.
- Correlation does not imply causation.
- Pearson correlation ranges between -1 and +1.
- Scatter plots are useful for assessing linearity.
- Regression introduces explanatory relationships.
- Residuals measure prediction error.
- R² measures explained variation.
- Hypothesis testing is essential when interpreting regression models.

<br>

The tutor also emphasised the importance of interpreting statistical findings within context rather than relying solely on numerical results.

<br>

---

<br>

## Seminar Activity – COVID-19 Correlation and Regression Analysis

<br>

The seminar activity used a small COVID-19 dataset to investigate correlation and regression concepts.

<br>

### Data Preparation

A new variable was created:

```text
TotalConfirmed =
ConfirmedIndianNational +
ConfirmedForeignNational
```

<br>

### Correlation Analysis

Pearson correlation coefficients were calculated between:

- TotalConfirmed and Cured.
- TotalConfirmed and Deaths.
- Cured and Deaths.

<br>

This activity demonstrated how correlation can be used to evaluate relationships between healthcare variables.

<br>

### Regression Analysis

A simple linear regression model was developed to predict the number of deaths using TotalConfirmed as the predictor variable.

<br>

The activity required interpretation of:

- Regression equation.
- Intercept.
- Slope coefficient.
- R² value.
- Adjusted R².
- F-statistic.
- Model p-value.
- Predictor significance.

<br>

This exercise strengthened my understanding of predictive analytics and how regression models can be interpreted in practical contexts.

<br>

---

<br>

## Seminar Recording Learning

<br>

The seminar recording provided additional insight into statistical analysis, assignments, and practical use of R.

<br>

Key lessons included:

- Correlation does not establish cause-and-effect relationships.
- Regression introduces directional relationships between variables.
- Scatter plots should be examined before fitting regression models.
- R can be learned progressively through practical application rather than memorisation.
- Seminar code can be adapted and reused for assignments when appropriately acknowledged.
- Statistical analysis should combine calculations with interpretation and critical thinking.
- The e-portfolio provides evidence for the final reflective assessment.

<br>

The tutor also highlighted the importance of hypothesis testing, statistical significance, confidence levels, and responsible interpretation of findings.

<br>

---

<br>

## Activities Completed

<br>

- Reviewed Unit 10 lecture materials.
- Studied correlation concepts and terminology.
- Learned about Pearson correlation coefficients.
- Explored positive, negative, and zero correlation.
- Studied scatter plots and visualisation techniques.
- Reviewed independent and dependent variables.
- Learned how to perform correlation analysis in R.
- Studied simple linear regression.
- Reviewed multiple regression concepts.
- Completed Data Activity 8 using the Health_Data dataset.
- Attended and reviewed the Unit 10 seminar.
- Completed the COVID-19 correlation activity.
- Reviewed regression analysis and model interpretation.
- Studied residuals, R², and adjusted R².
- Examined model and predictor significance.
- Reviewed assignment and e-portfolio guidance.

<br>

---

<br>

## Reflection

One of the most valuable lessons from Unit 10 was learning the distinction between correlation and regression. Although both techniques examine relationships between variables, I now understand that correlation measures association while regression attempts to explain and predict outcomes.

<br>

The Health_Data activity provided practical experience in calculating correlation coefficients and interpreting scatter plots. This demonstrated how statistical measures and visualisation techniques work together when analysing data.

<br>

The seminar further strengthened my understanding by emphasising that statistical findings must be interpreted in context. Numerical results alone are not sufficient; analysts must understand the meaning behind the results and the assumptions upon which they are based.

<br>

The discussion of regression modelling and R² was particularly useful because predictive models are widely used throughout Artificial Intelligence, Data Science, and business analytics. Understanding how much variation is explained by a model is essential when evaluating its performance and usefulness.

<br>

From a professional perspective, I can apply these techniques when analysing automation performance, application behaviour, operational KPIs, service-management data, and incident trends. Correlation and regression provide valuable tools for identifying patterns, explaining behaviour, and supporting evidence-based decisions.

<br>

Overall, Unit 10 strengthened my understanding of correlation analysis, regression modelling, statistical interpretation, and predictive analytics. These skills form an important foundation for more advanced analytical methods used in Artificial Intelligence, Machine Learning, and enterprise data analysis.

<br>

---

<br>

## References

<br>

Bader, M.K.F. and Leuzinger, S. (2024) *R-ticulate: A Beginner’s Guide to Data Analysis for Natural Scientists*. Hoboken, NJ: Wiley.

<br>

Field, A., Miles, J. and Field, Z. (2012) *Discovering Statistics Using R*. London: Sage Publications.

<br>

Li, Q. (2018) *Using R for Data Analysis in Social Sciences: A Research Project-Oriented Approach*. Oxford: Oxford University Press.

<br>

Pallant, J. (2020) *SPSS Survival Manual: A Step-by-Step Guide to Data Analysis Using IBM SPSS*. 7th edn. London: McGraw-Hill Education.

<br>

R Core Team (2025) *R: A Language and Environment for Statistical Computing*. Vienna: R Foundation for Statistical Computing.

<br>

University of Essex Online (2026) *Numerical Analysis: Unit 10 – Correlation and Regression*. MSc Artificial Intelligence Module Materials.
