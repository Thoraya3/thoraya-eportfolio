# Numerical Analysis – Unit 8 Reflection

## What? (Description)

In Unit 8 of Numerical Analysis, I studied nonparametric statistical tests and learned how they can be used when the assumptions required for parametric testing are not satisfied. In particular, nonparametric tests may be appropriate when quantitative data is not normally distributed, when substantial outliers are present, or when variables are measured using nominal or ordinal scales.

The unit built directly on Unit 7, where I studied parametric techniques such as the independent-samples t-test, paired t-test, and one-way ANOVA. Unit 8 introduced the corresponding nonparametric alternatives:

- Mann-Whitney U test as an alternative to the independent-samples t-test.
- Wilcoxon signed-rank test as an alternative to the paired t-test.
- Kruskal-Wallis test as an alternative to one-way ANOVA.
- Spearman’s rank correlation as an alternative to Pearson’s correlation when the relevant parametric assumptions are not satisfied.
- Chi-square test of independence for assessing associations between categorical variables.

The unit used the Health Data dataset to demonstrate how nonparametric tests can be performed and interpreted in R. I reviewed the assumptions and applications of the Mann-Whitney U, Wilcoxon signed-rank, and Kruskal-Wallis tests and considered how p-values are used to reach statistical decisions.

I also completed Data Activity 6, which involved calculating descriptive statistics for age and selecting appropriate statistical tests to compare blood-pressure measurements between participant groups. The scenario-based exercise introduced the use of sample means and 95% confidence intervals to compare employee-efficiency scores across three training vendors.

The Unit 8 seminar, titled *Selecting the Appropriate Statistical Test*, focused on identifying the correct test from the data type, number of groups, relationship between observations, and assumptions of the analysis. The seminar activity used a sales-forecasting dataset to compare paired and independent observations and reinforced the importance of stating null and alternative hypotheses before analysing results.

---

## So What? (Interpretation)

Unit 8 helped me understand that statistical tests should not be selected simply because they are familiar or convenient. The selection must be based on the research question, measurement scale, number of groups, independence of observations, distribution of the data, and assumptions associated with the test.

The distinction between parametric and nonparametric analysis was particularly valuable. Parametric tests generally analyse data using assumptions about population distributions and parameters such as means and variances. Nonparametric tests use ranks, signs, frequencies, or ordering and are useful when these assumptions are inappropriate. However, nonparametric tests are not assumption-free and may have less statistical power than appropriate parametric tests.

The unit also improved my understanding of paired and independent data. Paired observations are related, such as measurements collected from the same individuals before and after training. Independent observations come from separate and unrelated groups. Treating paired data as independent, or independent data as paired, can produce an invalid analysis.

This distinction is relevant to my work as a Senior Application Programmer in telecommunications. For example, comparing the performance of the same automation process before and after an optimisation would involve paired data. Comparing execution times from two separate automation platforms or independent service groups would involve independent data. Selecting the wrong comparison method could lead to an incorrect operational conclusion.

The seminar also reinforced the difference between descriptive and inferential statistics. Sample means may differ numerically even when there is insufficient evidence that the corresponding population values differ. A statistical test considers the observed difference relative to the variability and sample size before a population-level conclusion is made.

Unit 8 further strengthened my understanding of the p-value decision rule. When a p-value is less than the selected significance level, commonly 0.05, the null hypothesis is rejected. When it is greater than 0.05, the appropriate conclusion is to fail to reject the null hypothesis. Failing to reject the null hypothesis does not prove that the groups are identical. It means that the sample does not provide sufficient evidence of a statistically significant difference.

---

## What Next? (Action)

Going forward, I will use a structured process when selecting a statistical test:

1. Define the research question.
2. Identify the dependent and independent variables.
3. Determine whether the variables are categorical, ordinal, discrete, or continuous.
4. Identify the number of groups being compared.
5. Determine whether the observations are paired or independent.
6. Examine the distribution and possible outliers.
7. Select a parametric or nonparametric test.
8. State the null and alternative hypotheses.
9. Apply the test and compare the p-value with the significance level.
10. Interpret the result in the context of the original question.

I plan to practise both parametric and nonparametric methods in R and compare their results where appropriate. I will also improve my reporting by presenting the test selected, reason for selection, hypotheses, test statistic, p-value, effect direction, descriptive statistics, and contextual conclusion.

Within my professional role, I intend to apply this decision process when analysing automation performance, processing times, service incidents, application-response data, and operational survey results. This will help me avoid selecting statistical techniques without first checking whether the assumptions and data structures support their use.

The seminar also demonstrated that the unit activities contribute directly to the end-of-module statistical analysis assessment. I will therefore preserve relevant R code, interpretations, exercises, and reflections in my GitHub e-portfolio as evidence of the development of my analytical skills.

---

## Unit 8 Artefacts (My Submitted Work)

### 1. Comparison of Parametric and Nonparametric Tests

The unit introduced the following relationships between common parametric and nonparametric methods:

| Analytical purpose | Parametric method | Nonparametric method |
|---|---|---|
| Compare two independent groups | Independent-samples t-test | Mann-Whitney U test |
| Compare two related measurements | Paired t-test | Wilcoxon signed-rank test |
| Compare three or more independent groups | One-way ANOVA | Kruskal-Wallis test |
| Examine association between numerical variables | Pearson’s correlation | Spearman’s rank correlation |
| Examine association between categorical variables | Not a direct parametric equivalent | Chi-square test of independence |

This comparison helped me recognise that test selection depends on the structure and properties of the data rather than simply the number of variables available.

---

### 2. Mann-Whitney U Test

The Mann-Whitney U test compares two independent groups when the assumptions of an independent-samples t-test are not appropriate.

In the Health Data example, the research question was whether systolic blood-pressure values differed between the two sex categories.

The hypotheses were:

\[
H_0:
\text{The distributions or typical systolic blood-pressure values do not differ between the groups.}
\]

\[
H_1:
\text{The distributions or typical systolic blood-pressure values differ between the groups.}
\]

The R command was:

```r
wilcox.test(
  sbp ~ sex_1,
  data = Health_Data
)
```

The supplied result was:

```text
W = 5705.5
p-value = 0.1682
```

Using:

\[
\alpha=0.05
\]

the comparison is:

\[
0.1682>0.05
\]

Therefore, the decision is:

\[
\text{Fail to reject }H_0
\]

The sample does not provide sufficient evidence of a statistically significant difference in systolic blood pressure between the two groups.

This does not prove that the population values are exactly equal. It means that the available sample evidence is insufficient to establish a difference at the 5% significance level.

---

### 3. Wilcoxon Signed-Rank Test

The Wilcoxon signed-rank test compares two related measurements when the paired differences are not suitable for a paired t-test. A common example is comparing measurements collected from the same participants before and after an intervention.

In the Health Data example, the research question was whether participants’ post-test scores differed from their pre-test scores following training.

The hypotheses were:

\[
H_0:
\text{The typical paired difference between post-test and pre-test scores is zero.}
\]

\[
H_1:
\text{The typical paired difference between post-test and pre-test scores is not zero.}
\]

The R command was:

```r
wilcox.test(
  Health_Data$pre_test,
  Health_Data$post_test,
  paired = TRUE,
  exact = FALSE
)
```

The supplied output was:

```text
V = 0
p-value = 8.288e-07
```

The scientific notation means:

\[
8.288\times10^{-7}=0.0000008288
\]

This value is much smaller than:

\[
0.05
\]

Therefore:

\[
\text{Reject }H_0
\]

There is statistically significant evidence of a difference between the pre-test and post-test scores.

#### Accuracy note

The supplied Unit 8 notes state that this p-value is greater than 0.05 and conclude that the training was not effective. This interpretation is mathematically incorrect. The reported p-value is substantially less than 0.05, so the null hypothesis should be rejected.

The test establishes a statistically significant change, but the direction and practical size of that change should be confirmed by examining the pre-test and post-test descriptive statistics and paired differences.

---

### 4. Kruskal-Wallis Test

The Kruskal-Wallis test compares three or more independent groups when the assumptions of one-way ANOVA are inappropriate. It analyses ranks rather than the original numerical values.

In the Health Data example, the research question was whether systolic blood pressure differed across religious groups.

The hypotheses were:

\[
H_0:
\text{The distributions or mean ranks of systolic blood pressure are the same across the groups.}
\]

\[
H_1:
\text{At least one group differs from another.}
\]

The R command was:

```r
kruskal.test(
  sbp ~ religion,
  data = Health_Data
)
```

The supplied result was:

```text
Kruskal-Wallis chi-squared = 0.054144
df = 2
p-value = 0.9733
```

Because:

\[
0.9733>0.05
\]

the decision is:

\[
\text{Fail to reject }H_0
\]

The sample does not provide sufficient evidence that the distribution of systolic blood pressure differs across the religious groups.

If the Kruskal-Wallis result had been statistically significant, a suitable post-hoc procedure would have been required to identify which groups differed. The overall Kruskal-Wallis result alone would not identify the specific pairs responsible for the difference.

---

### 5. Data Activity 6: Analysis of the Health Data Dataset

Data Activity 6 required the application of descriptive statistics and nonparametric tests to the Health Data dataset.

#### Task 1: Mean, Median, and Mode of Age

The mean and median can be calculated in R using:

```r
mean(
  Health_Data$age,
  na.rm = TRUE
)

median(
  Health_Data$age,
  na.rm = TRUE
)
```

Base R does not provide a direct statistical mode function, because `mode()` in R refers to the storage mode of an object. A custom function can be used:

```r
statistical_mode <- function(x) {
  x <- na.omit(x)
  frequency <- table(x)
  modes <- as.numeric(
    names(frequency)[frequency == max(frequency)]
  )
  return(modes)
}

statistical_mode(Health_Data$age)
```

The results should be reported as:

```text
Mean age: [insert R output]
Median age: [insert R output]
Mode age: [insert R output]
```

The mean describes the arithmetic average, the median describes the middle observation, and the mode identifies the most frequently observed age.

#### Task 2: Diastolic Blood Pressure by Diabetes Status

The task asked whether median diastolic blood pressure was the same among diabetic and non-diabetic participants.

Because there are two independent groups and the measurement is being analysed nonparametrically, the appropriate method is the Mann-Whitney U test, implemented in R through the Wilcoxon rank-sum test.

The hypotheses are:

\[
H_0:
\text{The distribution of diastolic blood pressure is the same across diabetes groups.}
\]

\[
H_1:
\text{The distribution of diastolic blood pressure differs across diabetes groups.}
\]

Example command:

```r
wilcox.test(
  dbp ~ diabetes,
  data = Health_Data,
  exact = FALSE
)
```

Group medians can be calculated using:

```r
aggregate(
  dbp ~ diabetes,
  data = Health_Data,
  FUN = median,
  na.rm = TRUE
)
```

The interpretation should follow this rule:

```text
If p < 0.05:
Reject H0. There is evidence of a statistically significant difference
in diastolic blood pressure between diabetic and non-diabetic participants.

If p >= 0.05:
Fail to reject H0. There is insufficient evidence of a statistically
significant difference between the groups.
```

#### Task 3: Systolic Blood Pressure across Occupational Groups

The task asked whether systolic blood pressure differed across occupational groups.

Because more than two independent groups are being compared through a nonparametric method, the appropriate test is Kruskal-Wallis.

The hypotheses are:

\[
H_0:
\text{The systolic blood-pressure distributions are the same across occupational groups.}
\]

\[
H_1:
\text{At least one occupational group differs.}
\]

Example R command:

```r
kruskal.test(
  sbp ~ occupation,
  data = Health_Data
)
```

Group summaries can be calculated using:

```r
aggregate(
  sbp ~ occupation,
  data = Health_Data,
  FUN = median,
  na.rm = TRUE
)
```

The interpretation should follow this rule:

```text
If p < 0.05:
Reject H0. At least one occupational group has a different systolic
blood-pressure distribution.

If p >= 0.05:
Fail to reject H0. There is insufficient evidence of a difference
across occupational groups.
```

If the Kruskal-Wallis test is significant, post-hoc pairwise comparisons would be required to establish which occupational groups differ.

#### Reflection on Data Activity 6

This activity strengthened my ability to connect a research question with an appropriate statistical technique. It also reinforced that descriptive statistics and inferential tests serve different purposes. Descriptive statistics summarise what is observed in the sample, while inferential tests assess whether the sample provides evidence of a population-level difference.

---

### 6. Scenario-Based Exercise: Vendor Training Efficiency

The scenario described an organisation that employed three vendors to deliver one-week training programmes. The objective was to calculate the mean efficiency score for each group and evaluate which vendor demonstrated the strongest improvement at the 95% level.

The scores supplied were:

```text
Vendor 1: 45, 29, 56, 52, 45, 45, 41

Vendor 2: 61, 53, 41, 58, 53, 47, 44

Vendor 3: 35, 21, 33, 27, 22, 26, 30
```

#### Data-quality observation

The instructions state that each group contains eight employees. However, only seven scores are shown for each vendor in the supplied table. This means that at least one score per group appears to be missing.

It would be inappropriate to invent the missing observations. The following calculations therefore use the seven displayed values and should be treated as provisional until the complete dataset is confirmed.

#### Mean Efficiency Scores from the Available Data

For Vendor 1:

\[
\bar{x}_1=
\frac{45+29+56+52+45+45+41}{7}
\]

\[
\bar{x}_1=
\frac{313}{7}
\]

\[
\bar{x}_1\approx44.71
\]

For Vendor 2:

\[
\bar{x}_2=
\frac{61+53+41+58+53+47+44}{7}
\]

\[
\bar{x}_2=
\frac{357}{7}
\]

\[
\bar{x}_2=51.00
\]

For Vendor 3:

\[
\bar{x}_3=
\frac{35+21+33+27+22+26+30}{7}
\]

\[
\bar{x}_3=
\frac{194}{7}
\]

\[
\bar{x}_3\approx27.71
\]

The provisional ranking is:

1. Vendor 2: 51.00
2. Vendor 1: 44.71
3. Vendor 3: 27.71

Vendor 2 has the highest observed sample mean.

#### Important Statistical Interpretation

The highest sample mean does not automatically demonstrate a statistically significant improvement. A valid statistical conclusion also requires information about:

- Variation within each group.
- Sample size.
- Baseline efficiency or a comparison value.
- Whether employee allocation was independent.
- Whether the scores satisfy the assumptions of the selected test.
- The complete eighth score for each group.

If the objective is to compare the post-training scores of three independent vendor groups, a one-way ANOVA may be appropriate when the assumptions are satisfied. A Kruskal-Wallis test may be suitable when those assumptions are not satisfied.

If actual before-and-after scores exist for each employee, a paired analysis should be conducted within each vendor group. Without baseline scores, the available data compares post-training efficiency across vendors but does not directly measure individual improvement.

#### Example R Code

```r
vendor1 <- c(
  45, 29, 56, 52, 45, 45, 41
)

vendor2 <- c(
  61, 53, 41, 58, 53, 47, 44
)

vendor3 <- c(
  35, 21, 33, 27, 22, 26, 30
)

mean(vendor1)
mean(vendor2)
mean(vendor3)

t.test(vendor1, conf.level = 0.95)
t.test(vendor2, conf.level = 0.95)
t.test(vendor3, conf.level = 0.95)
```

To compare the three independent groups:

```r
vendor_data <- data.frame(
  score = c(
    vendor1,
    vendor2,
    vendor3
  ),
  vendor = factor(
    rep(
      c(
        "Vendor 1",
        "Vendor 2",
        "Vendor 3"
      ),
      each = 7
    )
  )
)

kruskal.test(
  score ~ vendor,
  data = vendor_data
)
```

If normality and variance assumptions are supported:

```r
vendor_anova <- aov(
  score ~ vendor,
  data = vendor_data
)

summary(vendor_anova)
```

#### Scenario Conclusion

Based only on the seven displayed scores per group, Vendor 2 has the highest average post-training efficiency. However, the missing observations and absence of baseline scores prevent a complete conclusion about statistically significant improvement.

This exercise reinforced the importance of checking data completeness and ensuring that the statistical method matches the claim being investigated.

---

### 7. Unit 8 Seminar: Selecting the Appropriate Statistical Test

The Unit 8 seminar focused on selecting an appropriate statistical test from the research question, data types, assumptions, and relationship between observations.

The seminar questions addressed:

1. The types of data being measured.
2. Tests used to assess associations between variables.
3. Differences between paired and unpaired data.

#### Types of Data

The seminar distinguished between categorical and numerical data.

Categorical data includes:

- Nominal variables, where categories have no inherent order.
- Ordinal variables, where categories have a meaningful order.

Numerical data includes:

- Discrete variables, represented by countable values.
- Continuous variables, which can take values across a measurement scale.

In the Superstore dataset:

- Category and Segment are categorical variables.
- Sales is a continuous numerical variable.
- Customer ID is an identifier rather than a quantitative measurement.

#### Tests of Association

The appropriate test depends on the variables:

- Two categorical variables: chi-square test of independence.
- Two numerical variables with an approximately linear relationship: Pearson’s correlation.
- Ordinal or non-normal numerical variables with a monotonic relationship: Spearman’s rank correlation.
- One categorical variable with two groups and one numerical variable: independent or paired t-test, depending on the observations.
- One categorical variable with three or more groups and one numerical variable: ANOVA or Kruskal-Wallis.

#### Paired and Unpaired Data

Paired data contains linked observations. Examples include:

- The same participants measured before and after an intervention.
- The same customers’ spending in two product categories.

Unpaired data comes from separate, unrelated groups. Examples include:

- Consumer customers compared with corporate customers.
- Two different operational teams.
- Two independent customer populations.

---

### 8. Superstore Paired t-Test Activity

The first seminar analysis compared average Technology and Furniture spending among customers who purchased from both categories.

The hypotheses were:

\[
H_0:
\mu_{\text{Technology}}
=
\mu_{\text{Furniture}}
\]

\[
H_1:
\mu_{\text{Technology}}
\neq
\mu_{\text{Furniture}}
\]

The analysis used a paired t-test because the same customers contributed spending values to both categories.

The seminar reported:

```text
p-value = 0.1168
```

Because:

\[
0.1168>0.05
\]

the decision was:

\[
\text{Fail to reject }H_0
\]

There was insufficient evidence at the 5% significance level that average Technology spending differed from average Furniture spending across the relevant population.

Although the sample means were numerically different, the observed difference was not sufficiently large relative to its uncertainty to establish a statistically significant population difference.

---

### 9. Superstore Independent t-Test Activity

The second seminar analysis compared average sales between Consumer and Corporate customer segments.

The hypotheses were:

\[
H_0:
\mu_{\text{Consumer}}
=
\mu_{\text{Corporate}}
\]

\[
H_1:
\mu_{\text{Consumer}}
\neq
\mu_{\text{Corporate}}
\]

The observations came from separate customer groups, so an independent-samples test was appropriate.

The seminar reported a p-value of approximately:

```text
p-value = 0.5575
```

Because:

\[
0.5575>0.05
\]

the decision was:

\[
\text{Fail to reject }H_0
\]

The sample did not provide sufficient evidence of a statistically significant difference in average sales between Consumer and Corporate customer segments.

The seminar reinforced that different sample means do not automatically imply different population means.

---

### 10. Seminar Learning and Assignment Preparation

The seminar provided direct guidance for the end-of-module statistical analysis assignment.

The tutor emphasised that the assessment requires:

- Data exploration.
- Descriptive statistical analysis.
- Appropriate visualisations.
- Inferential statistical tests.
- Explicit null and alternative hypotheses.
- Correct interpretation of p-values.
- Clear conclusions in the context of the research question.
- Evidence of work and learning in the GitHub e-portfolio.

The session also demonstrated a practical R workflow:

- Import the dataset.
- Inspect its structure.
- Group and summarise observations.
- Filter the relevant subset.
- Transform data into an appropriate format.
- Calculate descriptive statistics.
- Run the selected statistical test.
- Interpret the test statistic, degrees of freedom, p-value, and confidence interval.

A key lesson was that successful analysis requires more than generating numerical output. The test must be justified, assumptions must be considered, hypotheses must be stated, and results must be interpreted clearly.

---

### 11. Activities Completed

- Reviewed the Unit 8 reading materials and notes.
- Studied the characteristics of nonparametric tests.
- Compared parametric and nonparametric methods.
- Reviewed the Mann-Whitney U test.
- Reviewed the Wilcoxon signed-rank test.
- Reviewed the Kruskal-Wallis test.
- Considered Spearman’s rank correlation and chi-square testing.
- Completed Data Activity 6 using the Health Data dataset.
- Reviewed the vendor training scenario and provisional efficiency calculations.
- Examined the role of 95% confidence intervals.
- Read the seminar article on choosing the correct statistical test.
- Reviewed categorical, ordinal, discrete, and continuous data.
- Compared paired and independent observations.
- Reviewed paired and independent t-tests using the Superstore dataset.
- Studied the tutor’s guidance on the statistical analysis assessment.
- Documented the learning process within the GitHub e-portfolio.

---

### 12. Seminar Notes

The seminar emphasised that the appropriate statistical test depends on:

- The research question.
- The number and type of variables.
- The scale of measurement.
- The number of groups.
- Whether groups are paired or independent.
- Whether parametric assumptions are satisfied.
- The type of association or difference being investigated.

The session also reinforced the importance of scientific reporting. A complete statistical analysis should state the hypotheses, justify the selected method, report descriptive and inferential results, and explain the conclusion in context.

Another important seminar lesson was that a sample-level difference does not automatically establish a population-level difference. Inference requires the observed difference to be considered alongside the sample variability, sample size, and statistical uncertainty.

---

### 13. Overall Reflection

One of the most valuable outcomes of Unit 8 was learning to approach statistical analysis as a decision process. Before this unit, it was easy to view statistical tests as separate formulas or R commands. Unit 8 demonstrated that the tests form a connected framework in which test selection depends on the question, variables, assumptions, and structure of the observations.

The Health Data activity strengthened my understanding of nonparametric comparisons. The Mann-Whitney U test, Wilcoxon signed-rank test, and Kruskal-Wallis test provided alternatives for situations where parametric assumptions are not appropriate.

The scenario-based exercise also highlighted the importance of data quality. Recognising that the vendor table stated eight employees but displayed only seven scores per group was an important analytical observation. Statistical calculations should not proceed by silently inventing or ignoring missing information.

The seminar further developed my ability to distinguish paired from independent data. This distinction is directly relevant to business and telecom analysis. For example, testing the same automation workflow before and after an upgrade requires a paired method, while comparing two independent customer groups requires an independent method.

The unit also reinforced accurate hypothesis-test language. A result with \(p>0.05\) should be described as failing to reject the null hypothesis rather than proving that the null hypothesis is true. Similarly, a statistically significant result should not automatically be interpreted as operationally important without considering effect size, confidence intervals, and business context.

Overall, Unit 8 improved my ability to select, apply, and interpret statistical tests. It also provided direct preparation for the end-of-module assessment by connecting descriptive statistics, inferential tests, R programming, visualisation, and critical interpretation.

---

## References

Bader, M.K.F. and Leuzinger, S. (2024) *R-ticulate: A Beginner’s Guide to Data Analysis for Natural Scientists*. Hoboken, NJ: Wiley.

Daniel, W.W. and Cross, C.L. (2018) *Biostatistics: A Foundation
