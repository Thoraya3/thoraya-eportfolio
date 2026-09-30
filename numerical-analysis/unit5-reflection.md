# Numerical Analysis – Unit 5 Reflection

## What? (Description)

In Unit 5 of Numerical Analysis, I learned how to create and customise different types of graphs and plots using R. The unit introduced a variety of data visualisation techniques and demonstrated how graphical representations can help communicate statistical information more effectively. I learned how to adjust axes, add labels and titles, use colours, and customise plots to improve data presentation and interpretation.

The unit also introduced the foundations of calculus, including differentiation and integration. I learned that differentiation focuses on rates of change while integration focuses on combining small quantities to determine accumulated values. The learning materials explained the importance of calculus in statistics, mathematical modelling, Artificial Intelligence, and Machine Learning.

As part of the unit, I completed a COVID-19 visualisation activity, explored different plotting techniques in R, reviewed introductory calculus materials through Khan Academy resources, and participated in the collaborative discussion on descriptive statistics and visualisation.

## So What? (Interpretation)

This unit demonstrated that data analysis is not only about generating statistical results but also about communicating findings effectively. Visualisation techniques allow information to be presented in a way that makes trends, patterns, and comparisons easier to understand. A well-designed chart can often communicate information more effectively than a large table containing numerous numerical values.

As a Senior Application Programmer working within the telecommunications industry, I regularly work with dashboards, KPI reports, service-monitoring statistics, automation reports, and operational performance indicators. Understanding data visualisation principles is extremely useful because it helps communicate analytical findings to both technical and non-technical stakeholders.

The introduction to calculus also provided valuable insight into the mathematical foundations of Artificial Intelligence and Machine Learning. Although the concepts were introductory, they highlighted how rates of change and optimisation are used in data modelling and predictive analytics.

The collaborative discussion reinforced the importance of presenting statistical findings clearly and supported the idea that visualisation and descriptive statistics are both essential components of effective decision-making.

## What Next? (Action)

Going forward, I plan to continue improving my visualisation skills using both R and Python. I will focus on selecting appropriate graph types based on the characteristics of the data and the intended audience.

I also intend to strengthen my understanding of calculus and its applications within optimisation, machine learning, and predictive analytics. Developing a stronger mathematical foundation will support future learning throughout the MSc Artificial Intelligence programme.

Within my professional role, I will continue applying visualisation techniques when producing automation reports, operational dashboards, service-monitoring reports, and management presentations. These skills will help support clearer communication and more effective decision-making.

## Unit 5 Artefacts (My Submitted Work)

### 1. Data Activity – COVID-19 India Dataset Visualisation

As part of Unit 5, I completed a practical visualisation activity using the COVID-19 India Dataset (January 2020 – March 2020).

The activity involved:

- Creating a bar chart showing the frequency of COVID-19 reports by state or union territory.
- Creating a pie chart using ConfirmedIndianNational and ConfirmedForeignNational variables.
- Creating a histogram showing the distribution of recovery numbers.
- Creating a line chart showing trends in total cases over time.
- Interpreting the visual patterns and trends displayed within the data.

Example R commands used:

```r
barplot(table(State_UnionTerritory))

pie(case_totals)

hist(Cured)

plot(Date, TotalCases, type="l")
```

This activity improved my understanding of how visualisation techniques can be applied to real-world datasets and demonstrated how graphical representations can support data interpretation and communication.

### 2. Collaborative Discussion – Application of Descriptive Statistics and Visualisation

#### Initial Post Submitted

When reviewing the editor’s feedback regarding Table 2 in Brown (1994), I agree that large statistical tables can often be difficult for readers to interpret. While tables provide detailed numerical information, they may overwhelm readers when too much information is presented at once. Data visualisation offers a more effective way of communicating statistical findings because patterns, trends, and comparisons can be identified more quickly through graphical representation (Tufte, 2001; Few, 2013).

To improve the presentation of Table 2, I would replace sections of the table with a combination of bar charts, pie charts, and line graphs. A bar chart would allow readers to compare categories easily, while a line chart would demonstrate changes and trends over time. Pie charts could also be used where proportions need to be communicated. These visualisations reduce cognitive effort and allow readers to focus on key findings rather than searching through large quantities of numerical data (Knaflic, 2015).

One important lesson from this activity is that statistical analysis is not only about producing accurate calculations but also about presenting results in a way that supports understanding and decision-making. Descriptive statistics such as frequencies, percentages, means, and distributions become more meaningful when supported by appropriate visualisations. Poor presentation can obscure important findings, while effective visualisation can improve communication and promote better interpretation of results (Cairo, 2019).

During this exercise, I also realised the importance of selecting the correct visualisation for the intended audience. Histograms are effective for showing distributions, bar charts support comparisons, and line graphs are useful for illustrating trends. Choosing the wrong visualisation may confuse readers or lead to incorrect interpretation of the data (Few, 2013).

In my professional role within the telecommunications industry, visualisation is frequently used within dashboards, automation reports, KPI monitoring, and operational performance management. This activity reinforced the importance of presenting statistical findings in a format that is clear and accessible to both technical and non-technical stakeholders. Overall, I learned that effective visualisation enhances communication, improves interpretation, and increases the practical value of statistical analysis.

#### Reflection on the Discussion

This discussion helped me understand that effective statistical communication is as important as the statistical calculations themselves. Presenting data through charts and visualisations can significantly improve understanding and allow decision-makers to identify trends and patterns more efficiently.

The activity strengthened my ability to critically evaluate statistical presentation methods and reinforced the importance of selecting visualisations that match both the data and the target audience.

As someone working within telecommunications and automation, I regularly work with dashboards and reports that must communicate complex information clearly. This discussion reinforced the value of visual communication and its role in supporting effective decision-making.

### 3. Activities Completed

- Reviewed Unit 5 lecture materials and notes.
- Learned how to create and customise graphs and plots using R.
- Explored different visualisation methods and their applications.
- Studied differentiation and integration concepts.
- Completed Khan Academy calculus learning activities.
- Completed the COVID-19 visualisation activity.
- Participated in the collaborative discussion.
- Explored the role of visualisation in reporting and decision-making.

### 4. Seminar Notes

The seminar preparation focused on graphical representation of data and the importance of selecting suitable visualisation techniques. The materials highlighted how graphs improve interpretation and how calculus contributes to mathematical modelling, machine learning, and Artificial Intelligence.

### 5. Reflection

One of the most valuable lessons from Unit 5 was understanding that visual representation is a critical part of effective data analysis. Graphs and charts make complex information easier to interpret and improve communication of statistical findings.

The COVID-19 visualisation activity demonstrated how different visualisations reveal different aspects of the same dataset, while the collaborative discussion showed how visualisation can improve the presentation of statistical findings.

The introduction to calculus provided a useful foundation for understanding optimisation and modelling techniques used in Artificial Intelligence and Machine Learning. Overall, Unit 5 strengthened both my analytical and communication skills and highlighted the importance of presenting data effectively.

## References

Brown, S. (1994) *Article provided in Unit 5 reading materials*.

Cairo, A. (2019) *How Charts Lie: Getting Smarter about Visual Information*. New York: W.W. Norton & Company.

Few, S. (2013) *Information Dashboard Design: Displaying Data for At-a-Glance Monitoring*. 2nd edn. Burlingame, CA: Analytics Press.

Field, A., Miles, J. and Field, Z. (2012) *Discovering Statistics Using R*. London: Sage Publications.

James, G., Witten, D., Hastie, T. and Tibshirani, R. (2021) *An Introduction to Statistical Learning*. 2nd edn. New York: Springer.

Knaflic, C.N. (2015) *Storytelling with Data: A Data Visualization Guide for Business Professionals*. Hoboken, NJ: Wiley.

Pallant, J. (2020) *SPSS Survival Manual: A Step-by-Step Guide to Data Analysis Using IBM SPSS*. 7th edn. London: McGraw-Hill Education.

R Core Team (2025) *R: A Language and Environment for Statistical Computing*. Vienna: R Foundation for Statistical Computing.

Tufte, E.R. (2001) *The Visual Display of Quantitative Information*. 2nd edn. Cheshire, CT: Graphics Press.

University of Essex Online (2026) *Numerical Analysis: Unit 5 – Producing Plots and Introducing Calculus*. MSc Artificial Intelligence Module Materials.
