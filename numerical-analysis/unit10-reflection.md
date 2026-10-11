# Numerical Analysis – Unit 10 Reflection

<br>

## What? (Description)

In Unit 10 of Numerical Analysis, I studied correlation and regression analysis. The unit focused on understanding the relationship between variables, measuring the strength and direction of associations, and predicting outcomes using regression models.

<br>

I learned that correlation is a statistical measure used to describe the relationship between two variables. Correlation analysis helps determine both the strength and direction of the relationship, while regression analysis extends this idea by modelling how changes in one variable can be used to predict changes in another.

<br>

The lecture materials introduced the concepts of independent and dependent variables, scatter plots, Pearson’s correlation coefficient, simple linear regression, and multiple linear regression.

<br>

I learned that Pearson’s correlation coefficient, represented by **r**, ranges from -1 to +1.

<br>

- r = +1 indicates a perfect positive correlation.
- r = -1 indicates a perfect negative correlation.
- r = 0 indicates no linear relationship.

<br>

The lecturecast also demonstrated how scatter plots can be used to visualise relationships between variables and how regression models can be used to explain variability within a dependent variable.

<br>

As part of Data Activity 8, I used the Health_Data dataset to investigate the correlation between systolic and diastolic blood pressure and produce a scatter plot to visualise the relationship.

<br>

The Unit 10 seminar expanded on these concepts by focusing on correlation coefficients, regression line construction, residual analysis, model interpretation, and the distinction between correlation and causation.

<br>

---

<br>

## So What? (Interpretation)

Unit 10 helped me understand that correlation and regression are related but fundamentally different analytical techniques.

<br>

Correlation measures the strength and direction of an association between two variables. Importantly, correlation does not imply causation. Two variables may be strongly correlated without one causing the other.

<br>

The seminar reinforced that a correlation coefficient only measures association and remains unchanged whether Variable A is correlated with Variable B or Variable B is correlated with Variable A. Regression, however, introduces direction and attempts to explain how changes in an independent variable influence a dependent variable.

<br>

One of the most important lessons from the seminar was understanding the difference between association and causation. The tutor emphasised that correlation alone is insufficient for making population-level claims and that statistical testing and interpretation must accompany any findings.

<br>

I also learned how R² is used to evaluate regression models. An R² value represents the proportion of variation in the dependent variable that is explained by the regression model. For example, an R² value of 0.85 indicates that 85% of the variation in the outcome variable is explained by the predictor variables included in the model.

<br>

As a Senior Application Programmer working in telecommunications, these concepts are highly relevant. Correlation analysis can help identify relationships between system performance indicators, incident volumes, application response times, and automation outcomes. Regression models can then be used to predict operational performance, service demand, or other business outcomes.

<br>

The seminar also strengthened my understanding of hypothesis testing within regression analysis. I learned that regression coefficients must be tested for significance before meaningful population-level conclusions can be drawn.

<br>

---

<br>

## What Next? (Action)

Going forward, I plan to continue developing my understanding of correlation and regression analysis by practising the techniques in R using different datasets.

<br>

I will focus on:

- Producing and interpreting scatter plots.
- Calculating Pearson correlation coefficients.
- Applying simple linear regression models.
- Understanding residual analysis.
- Evaluating R² and adjusted R² values.
- Interpreting regression coefficients.
- Testing model significance using p-values and F-statistics.

<br>

Within my professional role, I intend to apply correlation and regression analysis when analysing service performance, automation efficiency, application behaviour, support metrics, and operational trends.

<br>

I will also continue documenting statistical exercises, code, visualisations, and reflections within my GitHub e-portfolio to support both assignment work and future professional development.

<br>

---

<br>

## Data Activity 8 – Correlation Analysis Using Health_Data

<br>

Data Activity 8 required analysis of the Health_Data dataset.

<br>

### Task 1: Correlation between Systolic and Diastolic Blood Pressure

<br>

The objective was to calculate the correlation between systolic blood pressure and diastolic blood pressure.

<br>

An example R command for performing this analysis is:

```r
cor(
  Health_Data$sbp,
  Health_Data$dbp,
  use = "complete.obs"
)
