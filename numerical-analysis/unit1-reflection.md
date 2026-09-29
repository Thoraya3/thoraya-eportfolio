# Numerical Analysis – Unit 1 Reflection

## What? (Description)

In Unit 1 of Numerical Analysis, I was introduced to the foundations of statistics, data analysis, and the R programming environment. The unit explored the importance of statistics in business, healthcare, sports, law, and many other fields, highlighting how statistical evidence can support decision making but may also be misleading if data sources and methods are not carefully examined.

The unit focused on understanding different types and sources of data, the distinction between descriptive and inferential statistics, and the importance of evaluating how data is collected and interpreted. I learned about the four levels of measurement commonly used in statistics: nominal, ordinal, interval, and ratio scales. The unit also introduced data manipulation, calculation, and graphical display within R.

A practical component of the unit involved learning to use R and RStudio, including installing the software, understanding the interface, importing and saving datasets, and performing initial data exploration. I also worked with a real-world COVID-19 India Cases dataset, which provided practical experience in loading data, examining dataset structures, identifying variable types, and understanding how statistical datasets are organised.

In addition to the lecturecasts and reading materials, I completed the required activities, explored the Module Wiki, participated in seminar preparation, and began building the Numerical Analysis section of my GitHub e-portfolio.

## So What? (Interpretation)

This unit reinforced the idea that effective analysis begins long before calculations are performed. Understanding where data originates, how it is collected, and how variables are measured is essential for producing reliable conclusions. The unit demonstrated that statistics is not simply about formulas but about critically evaluating evidence and making informed decisions.

As a Senior Application Programmer in the telecommunications industry, I frequently work with customer requests, operational reports, automation logs, and service performance data. Understanding data structures, data types, and measurement scales is highly relevant because it directly affects the quality of reporting and decision making. Incorrect interpretation of data can lead to flawed conclusions, inaccurate reporting, and poor operational outcomes.

The introduction to R and RStudio was particularly useful because it provided practical tools that are widely used within Data Science and Artificial Intelligence. The COVID-19 dataset activity demonstrated how raw data can be transformed into meaningful information through structured exploration and analysis. It also showed how statistical software can support evidence-based decision making using real-world datasets.

The concepts introduced in this unit provide an important foundation for later topics such as probability, data structures, statistical distributions, confidence intervals, hypothesis testing, and machine learning. Understanding these fundamentals is critical for developing strong analytical skills and applying data-driven methods effectively.

## What Next? (Action)

Going forward, I plan to continue strengthening my skills in R and RStudio by practising dataset exploration, data manipulation, and statistical analysis using real-world data. I will focus on becoming more confident in identifying data structures, understanding measurement scales, and selecting appropriate analytical techniques.

Within my professional role, I intend to apply these concepts when analysing telecom operational data, automation performance metrics, and business reporting datasets. Improving my understanding of data structures and statistical reasoning will help me make more informed decisions and support future work involving Artificial Intelligence and advanced analytics.

As I progress through the Numerical Analysis module, I will continue documenting my learning within my GitHub e-portfolio and connect each topic to practical applications within enterprise software development, automation, and telecommunications.

## Unit 1 Artefacts (My Submitted Work)

### 1. Data Activity – COVID-19 India Cases Dataset

As part of Unit 1, I worked with the COVID-19 India Cases dataset covering the period from January 2020 to March 2020. The objective of the activity was to gain practical experience in loading and exploring a real-world dataset using R and RStudio.

The activity involved:

- Downloading and saving the dataset in the R working directory.
- Importing the dataset into RStudio.
- Conducting an initial exploration of the dataset structure.
- Identifying the total number of variables and observations.
- Reviewing variable names and data types.
- Determining how many variables were numeric, character, and date types.
- Investigating the number of unique states and union territories represented.
- Identifying the reporting date range.
- Determining which state appeared most frequently in the dataset.

Example R commands used:

```r
str(covid_data)

nrow(covid_data)

ncol(covid_data)

names(covid_data)

summary(covid_data)
