# Numerical Analysis – Unit 2 Reflection

## What? (Description)

In Unit 2 of Numerical Analysis, I learned about data structures in R and their importance in managing and analysing data efficiently. The unit introduced different types of data structures used within R, including vectors, matrices, and data frames. I explored how data structures define the type of data stored, how the data is organised, and how it can be manipulated during statistical analysis.

The unit also covered the execution of commands in R and basic arithmetic operations such as addition, subtraction, multiplication, and division using various operators. Particular attention was given to vectors and matrices, including how mathematical operations can be performed on them.

The seminar focused on understanding descriptive statistics and their role in summarising and interpreting data.

## So What? (Interpretation)

This unit demonstrated that data structures are fundamental to any form of data analysis. Before statistical techniques can be applied, the data must be organised correctly and stored in appropriate structures.

As a Senior Application Programmer working in telecommunications, I regularly work with large volumes of operational and transactional data. The concepts covered in this unit helped me appreciate the importance of data organisation when developing reports, analysing service information, and building automation solutions.

The introduction to vectors and matrices was particularly valuable because these structures form the mathematical foundation for many Artificial Intelligence and Machine Learning algorithms.

## What Next? (Action)

Going forward, I plan to continue practising data manipulation in R to strengthen my understanding of vectors, matrices, and data frames. I also intend to build greater confidence in applying mathematical operations and statistical methods within R.

Within my professional role, I will look for opportunities to apply these concepts to telecom operations, automation reporting, and performance monitoring.

## Unit 2 Artefacts (My Submitted Work)

### 1. Data Activity – COVID-19 India Dataset

As part of Unit 2, I completed the COVID-19 India Dataset activity to explore how data structures and frequency analysis can be performed in R.

The activity focused on:

- Creating a frequency table using the `table()` function.
- Calculating percentages from frequency distributions.
- Creating a binary variable called `has_recovery`.
- Analysing recovery reporting patterns using frequency analysis.
- Exploring categorical data structures in R.

Example R commands used:

```r
has_recovery <- ifelse(Cured > 0, 1, 0)

table(has_recovery)

prop.table(table(has_recovery))*100
```

This activity demonstrated how raw data can be transformed into meaningful information using frequency analysis and descriptive statistics.

### 2. Activities Completed

- Reviewed Unit 2 lecturecast and learning materials.
- Learned about vectors, matrices, and data frames in R.
- Practised creating and manipulating data structures.
- Performed arithmetic operations using R operators.
- Completed the COVID-19 India Dataset activity.
- Created and analysed frequency tables.
- Created binary variables for statistical analysis.
- Reviewed Khan Academy mathematical resources.
- Participated in seminar preparation activities.

### 3. Seminar Notes

The seminar focused on understanding descriptive statistics and their role in data analysis. The session reinforced how data can be organised, summarised, and interpreted using statistical measures.

### 4. Reflection

One of the most useful lessons from Unit 2 was recognising that successful analysis depends heavily on how data is structured and managed. The unit demonstrated that statistical software relies on well-organised data structures to perform calculations accurately and efficiently.

The introduction to vectors and matrices also provided an important mathematical foundation that will support future topics within Numerical Analysis and Artificial Intelligence.

## References

Field, A., Miles, J. and Field, Z. (2012) *Discovering Statistics Using R*. London: Sage Publications.

Pallant, J. (2020) *SPSS Survival Manual*. 7th edn. London: McGraw-Hill Education.

R Core Team (2025) *R: A Language and Environment for Statistical Computing*. Vienna: R Foundation for Statistical Computing.

University of Essex Online (2026) *Numerical Analysis: Unit 2 – Data Structures in R*. MSc Artificial Intelligence Module Materials.
