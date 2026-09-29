# Numerical Analysis – Unit 3 Reflection

## What? (Description)

In Unit 3 of Numerical Analysis, I learned about data management in R and the importance of preparing datasets before statistical analysis can be performed. The unit focused on reading different types of data files into RStudio, examining datasets and variables, converting variable types, and managing missing values.

The lecture materials demonstrated how to inspect complete datasets and individual variables using R functions. I learned how different variable types influence analysis and why converting variables correctly is an important step when preparing data for statistical modelling. The unit also introduced methods for identifying and handling missing values, which is an essential skill when working with real-world datasets.

As part of the learning activities, I reviewed the reading materials, explored the recommended NumPy exercises for vectors and matrices, revised mathematical concepts covered in previous units, and completed the COVID-19 India Dataset activity. This activity involved creating new variables, performing frequency analysis, converting variables into factors, and analysing reporting patterns across Indian states and union territories.

## So What? (Interpretation)

This unit demonstrated that data management is one of the most important stages of data analysis. Even the most advanced statistical methods and Artificial Intelligence models can produce misleading results if datasets contain errors, inappropriate variable types, or missing information. The unit reinforced the idea that high-quality analysis depends on high-quality data preparation.

As a Senior Application Programmer working in the telecommunications industry, I frequently work with operational data, service requests, CRM records, automation logs, and reporting systems. Many of these datasets require data validation, transformation, and cleaning before they can be used for reporting and decision-making. The ability to examine variable structures, convert data types, and manage missing values is therefore highly relevant to my day-to-day responsibilities.

The activity using the COVID-19 dataset provided practical experience in creating new variables, categorising data, and producing frequency summaries. These are common tasks in business intelligence, reporting, and data science projects. The unit also highlighted how data preparation supports more advanced topics such as machine learning, predictive analytics, and statistical modelling.

The additional NumPy exercises reinforced the relationship between programming, numerical analysis, and linear algebra. This helped strengthen my understanding of how vectors and matrices are used in both statistical analysis and Artificial Intelligence applications.

## What Next? (Action)

Going forward, I plan to continue improving my ability to prepare and manage datasets using both R and Python. I will focus on strengthening my understanding of data cleaning, variable transformations, and missing-value handling because these skills are essential for successful data analysis projects.

Within my professional role, I intend to apply these techniques when analysing operational datasets, automation monitoring logs, and service performance reports. Improving my data management skills will help me produce more reliable analysis and support better decision-making within enterprise environments.

As I progress through the Numerical Analysis module, I will continue documenting my learning through my GitHub e-portfolio while linking statistical techniques and data management practices to real-world telecom and automation scenarios.

## Unit 3 Artefacts (My Submitted Work)

### 1. Data Activity – COVID-19 India Dataset

As part of Unit 3, I completed a practical activity using the COVID-19 India Dataset (January 2020 – March 2020). The purpose of the activity was to apply data management techniques within R and explore how variables can be transformed, categorised, and analysed.

The activity involved:

- Creating a binary variable called `has_deaths`.
- Assigning a value of 1 when deaths were reported.
- Assigning a value of 0 when no deaths were reported.
- Creating a frequency table using the `table()` function to analyse death-reporting patterns.
- Converting the binary variable into a factor variable using the labels:
  - No Deaths
  - Deaths Reported
- Creating a new categorical variable called `case_level`.
- Categorising reports into:
  - No Cases (0 cases)
  - Low Cases (1–5 cases)
  - Medium Cases (6–15 cases)
  - High Cases (16+ cases)
- Creating a frequency table for State/Union Territory reporting.
- Identifying the ten states with the highest number of daily reports.

Example R commands used:

```r
has_deaths <- ifelse(Deaths > 0, 1, 0)

table(has_deaths)

has_deaths <- factor(
  has_deaths,
  levels = c(0,1),
  labels = c("No Deaths","Deaths Reported")
)

table(State_UnionTerritory)

sort(table(State_UnionTerritory),
     decreasing = TRUE)
```

This activity demonstrated how raw data can be transformed into meaningful categories that support analysis and reporting. It also strengthened my understanding of variable conversion, factor variables, frequency analysis, and dataset preparation.

### 2. Activities Completed

- Reviewed Unit 3 lecturecast and reading materials.
- Explored data management techniques in R.
- Learned how to examine datasets and individual variables.
- Practised converting variable types.
- Studied methods of identifying and managing missing values.
- Completed the COVID-19 India Dataset activity.
- Created binary and categorical variables.
- Produced frequency tables and reporting summaries.
- Revised mathematical concepts from Units 1 and 2.
- Completed NumPy exercises covering vectors and matrices.
- Participated in formative learning activities.

### 3. Seminar Notes

The learning activities reinforced the importance of preparing and validating data before performing analysis. The materials demonstrated how variables can be converted, explored, categorised, and summarised within R while highlighting the importance of managing missing data. The practical exercises linked these concepts to real-world datasets and statistical reporting requirements.

### 4. Reflection

One of the most important lessons from Unit 3 was understanding that effective analysis depends on well-prepared data. Before statistical techniques can be applied, analysts must verify data quality, understand variable structures, and ensure that missing values and incorrect formats are handled appropriately.

The COVID-19 dataset activity provided valuable hands-on experience with data transformation and category creation. It demonstrated how real-world datasets often require preparation before meaningful insights can be extracted.

Overall, Unit 3 strengthened my confidence in working with datasets and provided practical skills that will support future topics such as probability distributions, confidence intervals, hypothesis testing, parametric tests, and statistical modelling.

## References

Field, A., Miles, J. and Field, Z. (2012) *Discovering Statistics Using R*. London: Sage Publications.

Harris, C.R. et al. (2020) ‘Array programming with NumPy’, *Nature*, 585(7825), pp. 357–362.

Pallant, J. (2020) *SPSS Survival Manual: A Step-by-Step Guide to Data Analysis Using IBM SPSS*. 7th edn. London: McGraw-Hill Education.

R Core Team (2025) *R: A Language and Environment for Statistical Computing*. Vienna: R Foundation for Statistical Computing. Available at: https://www.r-project.org/ (Accessed: 29 September 2026).

University of Essex Online (2026) *Numerical Analysis: Unit 3 – Data Management in R*. MSc Artificial Intelligence Module Materials.
