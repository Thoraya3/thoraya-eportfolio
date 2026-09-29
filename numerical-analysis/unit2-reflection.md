# Numerical Analysis – Unit 2 Reflection

## What? (Description)

In Unit 2 of Numerical Analysis, I learned about data structures in R and their importance in managing and analysing data efficiently. The unit introduced different types of data structures used within R, including vectors, matrices, and data frames. I explored how data structures define the type of data stored, how the data is organised, and how it can be manipulated during statistical analysis.

The unit also covered the execution of commands in R and basic arithmetic operations such as addition, subtraction, multiplication, and division using various operators. Particular attention was given to vectors and matrices, including how mathematical operations can be performed on them. The lecture materials demonstrated how R can be used to create, manipulate, and analyse these structures.

As part of the learning activities, I reviewed the lecturecast, completed the reading materials on data frames and their operations, explored the Khan Academy mathematics resources, and completed the Data Activity exercises. The seminar focused on understanding descriptive statistics and their role in summarising and interpreting data.

## So What? (Interpretation)

This unit demonstrated that data structures are fundamental to any form of data analysis. Before statistical techniques can be applied, the data must be organised correctly and stored in appropriate structures. Understanding vectors, matrices, and data frames provided insight into how analytical software stores and processes information behind the scenes.

As a Senior Application Programmer working in the telecommunications industry, I regularly work with large volumes of operational and transactional data. The concepts covered in this unit helped me appreciate the importance of data organisation when developing reports, analysing service information, and building automation solutions. Many of the structures discussed in R have similarities with the collections, arrays, tables, and datasets used within enterprise systems and databases.

The introduction to vectors and matrices was particularly valuable because these structures form the mathematical foundation for many Artificial Intelligence and Machine Learning algorithms. Understanding how mathematical operations are performed on structured data will help me as I progress to more advanced topics such as probability, hypothesis testing, statistical modelling, and AI algorithms.

The seminar on descriptive statistics also reinforced the importance of summarising data correctly before attempting more advanced analysis. Understanding central tendency, variability, and data organisation provides the basis for evidence-based decision making in both academic and professional environments.

## What Next? (Action)

Going forward, I plan to continue practising data manipulation in R to strengthen my understanding of vectors, matrices, and data frames. I also intend to build greater confidence in applying mathematical operations and statistical methods within R, as these skills will be required throughout the remainder of the Numerical Analysis module.

From a professional perspective, I will look for opportunities to apply these concepts to data used within telecom operations, automation reporting, and performance monitoring. Understanding data structures more deeply will help me work more effectively with analytical solutions and support future learning in Artificial Intelligence and Data Science.

As I progress through the module, I will continue documenting my learning within my GitHub e-portfolio while connecting the statistical concepts learned in this module to practical applications within enterprise software development and automation projects.

## Unit 2 Artefacts (My Submitted Work)

### 1. Data Activity – COVID-19 India Dataset

As part of Unit 2, I completed the COVID-19 India Dataset activity to explore how data structures and frequency analysis can be performed in R. The activity focused on creating and analysing a binary recovery indicator using COVID-19 reporting data from January 2020 to March 2020.

The activity required me to:

- Create a frequency table showing the number of daily reports that included recoveries and those that reported no recoveries.
- Calculate percentages to determine the proportion of reports containing recovery cases.
- Create a binary variable called `has_recovery` indicating whether any cured cases were reported.
- Apply frequency analysis techniques using R functions.
- Explore how data frames can be manipulated and summarised within R.

Example R commands used:

```r
has_recovery <- ifelse(Cured > 0, 1, 0)

table(has_recovery)

prop.table(table(has_recovery)) * 100
