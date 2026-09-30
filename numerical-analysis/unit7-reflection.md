# Numerical Analysis – Unit 7 Reflection

## What? (Description)

In Unit 7 of Numerical Analysis, I studied parametric statistical tests and their applications in data analysis. The unit focused on understanding the assumptions required before conducting parametric testing, particularly the assumption that data should be normally distributed. The learning materials introduced different forms of parametric statistical tests and demonstrated how these tests are performed using R.

The unit covered the Shapiro-Wilk normality test, One-Sample t-Test, Independent Two-Sample t-Test, Paired t-Test, and Analysis of Variance (ANOVA). I learned how each test is used to answer different research questions and how to interpret statistical outputs including p-values, confidence intervals, test statistics, degrees of freedom, and significance levels.

The Health Data dataset was used throughout the unit to perform normality testing and statistical analysis. In addition to the practical analytical activities, I completed the Summary Post for the collaborative discussion that started in Unit 5 and prepared for the Mathematics Test covering statistical and numerical analysis concepts from throughout the module.

---

## So What? (Interpretation)

This unit demonstrated how inferential statistics can be used to make decisions based on sample data. Parametric testing provides a structured framework for determining whether differences between groups or observations are statistically significant rather than simply the result of random variation.

As a Senior Application Programmer working in the telecommunications industry, I frequently work with operational metrics, service statistics, automation outcomes, and performance indicators. Understanding hypothesis testing and statistical significance allows me to interpret data more effectively and evaluate whether observed changes represent genuine improvement or random fluctuation.

The introduction to normality testing reinforced the importance of validating assumptions before selecting statistical methods. I learned that analytical techniques should be chosen based on the characteristics of the data rather than convenience. This concept is particularly relevant in professional environments where decisions must be based on reliable evidence.

The unit also strengthened my understanding of confidence intervals, significance testing, and the interpretation of p-values. These concepts are important foundations for Artificial Intelligence, Machine Learning, predictive analytics, and evidence-based decision-making.

---

## What Next? (Action)

Going forward, I plan to continue developing my statistical analysis skills by practising different hypothesis-testing techniques and interpreting statistical outputs. I will focus on selecting appropriate methods based on the nature of the data and the analytical question being investigated.

Within my professional role, I intend to apply statistical testing concepts when evaluating automation outcomes, service-performance data, operational reports, and business improvement initiatives. These analytical skills will help support more reliable and evidence-based decision-making.

As I continue through the MSc Artificial Intelligence programme, I will build upon these foundations by exploring advanced statistical modelling, predictive analytics, and machine learning techniques while continuing to document my learning in my GitHub e-portfolio.

---

## Unit 7 Artefacts (My Submitted Work)

### 1. Parametric Testing Activity Using Health Data

As part of Unit 7, I worked with the Health Data dataset to perform normality testing and parametric statistical analysis using R.

The activity included:

- Performing a Shapiro-Wilk normality test.
- Conducting a One-Sample t-Test.
- Conducting an Independent Two-Sample t-Test.
- Conducting a Paired t-Test.
- Performing One-Way ANOVA.
- Interpreting confidence intervals and p-values.
- Drawing conclusions based on statistical evidence.

Example R commands used:

```r
shapiro.test(Health_Data$sbp)

t.test(Health_Data$dbp, mu = 80)

t.test(age ~ diabetes,
data = Health_Data,
var.equal = TRUE)

t.test(before, after,
paired = TRUE)

res.aov <- aov(
income ~ religion_2,
data = Health_Data
)

summary(res.aov)
```

This activity strengthened my understanding of statistical testing procedures and improved my ability to interpret analytical results produced by R.

---

### 2. Collaborative Discussion – Summary Post

#### Summary Post Submitted

Reflecting on my initial post and the feedback received from my peers, I continue to support the view that large statistical tables should be simplified when they become difficult to interpret. However, the discussion helped me appreciate that visualisation is not simply about replacing tables with graphs. Rather, it is about selecting the most appropriate presentation method for both the data and the audience.

Several colleagues highlighted the importance of retaining key numerical values alongside graphical representations. I agree with this perspective because, while charts improve accessibility and help identify patterns quickly, detailed tables remain valuable when readers require exact numerical values. Therefore, an effective presentation often combines concise tables with suitable graphical visualisations (Few, 2013).

The peer discussions also reinforced the importance of choosing the correct type of graph. Following the comments from other students, I now recognise that some visualisations are more appropriate than others depending on the data structure and analytical objective. For example, bar charts generally allow more accurate comparisons than pie charts, while line graphs are most useful when data has a time-based dimension (Knaflic, 2015).

This discussion strengthened my understanding of how visualisation influences interpretation and decision-making. Effective presentation requires statistical accuracy, clarity, transparency, and accessibility. Poor visual design can result in misunderstanding regardless of the quality of the underlying analysis (Cairo, 2019).

From a professional perspective, this activity directly relates to my work within the telecommunications industry, where dashboards and operational reports communicate service performance, automation outcomes, and business metrics. The exercise reinforced the importance of presenting analytical findings in a way that supports informed decision-making.

Overall, this discussion improved my ability to critically evaluate statistical visualisations and demonstrated how peer feedback can strengthen analytical thinking and communication skills.

---

### 3. Mathematics Test

Unit 7 also included preparation for and completion of the Mathematics Test.

The test covered several topics studied throughout the module, including:

- Descriptive Statistics
- Quartiles and Interquartile Range (IQR)
- Outlier Detection
- Probability
- Confidence Intervals
- Hypothesis Testing
- Type I and Type II Errors
- Normal and t Distributions
- Vectors
- Cross Product
- Matrices
- Boxplots and Data Interpretation

The test provided an opportunity to apply the concepts learned throughout the module and demonstrated how statistical and mathematical techniques support analytical decision-making.

---

### 4. Activities Completed

- Reviewed Unit 7 lecture materials and notes.
- Studied normality testing and parametric assumptions.
- Learned how to perform One-Sample, Independent, and Paired t-Tests.
- Explored One-Way ANOVA.
- Worked with the Health Data dataset.
- Interpreted p-values, confidence intervals, and statistical outputs.
- Completed the Summary Post in the collaborative discussion.
- Prepared for and completed the Mathematics Test.
- Reviewed hypothesis testing and statistical significance concepts.

---

### 5. Seminar Notes

The seminar focused on hypothesis testing and statistical significance. The session reinforced the relationship between null and alternative hypotheses, p-values, confidence intervals, and decision-making.

The seminar highlighted the importance of assessing normality before selecting parametric statistical tests and demonstrated how significance testing can be used to support evidence-based conclusions.

The discussion of effect size and statistical significance also reinforced the need to consider both statistical and practical importance when evaluating analytical findings.

---

### 6. Reflection

One of the most valuable lessons from Unit 7 was understanding how statistical tests support objective decision-making. Parametric tests provide structured methods for assessing evidence and determining whether observed differences are statistically meaningful.

Working with the Health Data dataset provided practical experience with normality assessment, t-tests, and ANOVA analysis. The exercises strengthened my ability to interpret statistical outputs and increased my confidence in applying statistical reasoning to real-world problems.

The Summary Post encouraged me to reflect on feedback received from other students and demonstrated how collaborative learning can strengthen understanding. Reviewing different perspectives helped me refine my own thinking about data visualisation and statistical communication.

The Mathematics Test provided an opportunity to consolidate knowledge gained throughout the Numerical Analysis module and highlighted the connections between descriptive statistics, probability, hypothesis testing, confidence intervals, and mathematical reasoning.

Overall, Unit 7 strengthened my understanding of inferential statistics, hypothesis testing, and analytical decision-making while providing practical skills that are directly relevant to Artificial Intelligence, Data Science, and enterprise data analysis.

---

## References

Cairo, A. (2019) *How Charts Lie: Getting Smarter about Visual Information*. New York: W.W. Norton & Company.

Daniel, W.W. and Cross, C.L. (2018) *Biostatistics: A Foundation for Analysis in the Health Sciences*. Hoboken, NJ: Wiley.

Few, S. (2013) *Information Dashboard Design: Displaying Data for At-a-Glance Monitoring*. 2nd edn. Burlingame, CA: Analytics Press.

Field, A., Miles, J. and Field, Z. (2012) *Discovering Statistics Using R*. London: Sage Publications.

Kassambara, A. (2019) *Comparing Groups: Numerical Variables*.

Knaflic, C.N. (2015) *Storytelling with Data: A Data Visualization Guide for Business Professionals*. Hoboken, NJ: Wiley.

Levshina, N. (2015) *How to Do Linguistics with R: Data Exploration and Statistical Analysis*. Amsterdam: John Benjamins.

Pallant, J. (2020) *SPSS Survival Manual: A Step-by-Step Guide to Data Analysis Using IBM SPSS*. 7th edn. London: McGraw-Hill Education.

R Core Team (2025) *R: A Language and Environment for Statistical Computing*. Vienna: R Foundation for Statistical Computing.

Tufte, E.R. (2001) *The Visual Display of Quantitative Information*. 2nd edn. Cheshire, CT: Graphics Press.

University of Essex Online (2026) *Numerical Analysis: Unit 7 – Parametric Tests*. MSc Artificial Intelligence Module Materials.
