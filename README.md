# SAT Data: Analyzing test scores and participation rates from 2017-18

 - [Problem Statement](#Problem-Statement)
 - [Executive Summary](#Executive-Summary)
 - [sat-data-muhammad.ipynb contents](#sat-data-muhammad.ipynb-contents)
 - [Data Dictionary](#Data-Dictionary)
 - [External Research](#External-Research)
 - [Conclusions & Recommendations](#Conclusions-&-Recommendations)
 - [Data Sources](#Data-Sources)

## Problem Statement
In last couple of years, more than 2 million students took SAT in each year. This number confirm gaining greater access and opportunity<sup>1</sup>. In order to achieve success at large scale, questions to explore in such exams are: Does the SAT need to focus on increasing its participation rates? or The number of SAT test-takers can be increased by resources?

**Citations**:
<br>
<sup>1</sup> https://www.collegeboard.org/releases/2018/more-than-2-million-students-in-class-of-2018-took-sat-highest-ever

---
## Executive Summary
**INTRODUCTION**

An analysis is conducted on the SAT datasets. Each dataset contains state-by-state average test scores and participation rates, specifically from 2017 and 2018. Analyzing test scores and participation rates, the SAT make their test scores and participation data available to the public. 

**METHODOLOGY**

A **data science workflow** was implemented to conduct this analysis. Firstly, the **problem statement** was defined—the College Board needed to determine how to increase participation rates of the SAT. Next, **data scraping** was performed by locating credible sources that housed the appropriate datasets: SAT test scores and participation rates from 2017-18. Before beginning any analysis of the data, each individual dataset was imported to a **Pandas DataFrame**. Next, **data cleaning** was conducted to ensure that all datatypes were accurate and any other errors were fixed. Using all data from both years, an **exploratory data analysis** was conducted to determine any parameters. Since the SAT datasets contain data from an entire population of high school students from the class of 2017 and 2018, the population parameters were measured, not sample statistics. All statistical findings were used to then perform **data visualization**. The following data visualizations were used to display the data: 
- heat map
- histograms
- boxplots 
- scatterplots

Once all data was visualized and all statistical summaries were conveyed, **descriptive and inferential statistical analysis** was conducted to describe what the distributions were and any trends appeared in the data.  To confirm and support the observations made, **external research** about the SAT and any other relevant data was conducted. Finally, well-informed **data-driven recommendations** for the College Board were compiled. 

**SIGNIFICANT FINDINGS**

When analyzing the datasets, few findings about SAT test scores and participation rates were gathered. Here are the most significant findings, focusing primarily on the SAT: 
- SAT Total Scores, 2017-18: The distribution of average test scores from all states was bimodal. Students either performed very poorly or very well. 
- SAT Participation Rates, 2017-18: The distribution of participation rates from all states appeared to be right skewed and slightly bimodal, where a majority of states experienced low participation rates, and only some had high participation rates. 
- SAT Test Scores vs Participation Rates, 2017-18: In both years, there was a strong negative correlation between test scores and participation rates. The higher the participation rate, the lower the test score. A concentration of states on the East Coast tended have a combination of high participation and low test scores. 

### sat-data-muhammad.ipynb Contents:
- Description of the 2017 SAT data columns
- 2017 Data Import & Cleaning
- 2018 Data Import and Cleaning
- Exploratory Data Analysis
- Data Visualization
- Descriptive and Inferential Statistics
- External Research
- Conclusions and Recommendations
---
## Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*object*|sat_2017_csv|Names of all US states| 
|**sat_ewb_17**|*int*|sat_2017_csv|The mean score of the Evidence-Based Reading and Writing (ERW) category of the SAT in 2017 (score range: 200-800)|
|**sat_math_17**|*int*|sat_2017_csv|The mean score of the Math category of the SAT in 2017 (score range: 200-800)|
|**sat_total_17**|*int*|sat_2017_csv|The sum of the mean scores of ERW and Math in the SAT in 2017 (score range: 400-1600)|
|**sat_participation_17**|*float*|sat_2017_csv|The percentage of 2018 graduating seniors who took the SAT (0.9810 means 98.1%)|
|**sat_ewb_18**|*int*|sat_2018_csv|The mean score of the Evidence-Based Reading and Writing (ERW) category of the SAT in 2018 (score range: 200-800)|
|**sat_math_18**|*int*|sat_2018_csv|The mean score of the Math category of the SAT in 2018 (score range: 200-800)|
|**sat_total_18**|*int*|sat_2018_csv|The sum of the mean scores of ERW and Math in the SAT in 2018 (score range: 400-1600)|
|**sat_participation_18**|*float*|sat_2018_csv|The percentage of 2018 graduating seniors who took the SAT (0.9810 means 98.1%)|

---
## External Research
Around 2 million students from the class of 2018 took the SAT, the highest ever.$^{1}$ In fact, there was a 27% increase in participation rates from the previous year.$^{2}$ SAT participation rates are so high that as of 2018, the test holds the title for "most widely used college admission test," beating the ACT where 1.91 million students took that test in the same year.$^{3}$  Although the SAT can celebrate this achievement, the data shows that there is a negative correlation between participation rates and test scores. This means that the higher the participation rate amongst all states the lower the average student test scores. 

Contrary to the College Board's claim that the SAT offers "greater access and opportunity" for students who take their test. But the higher the chances are of more students performing poorly. If taking the SAT is a significant contributor to college acceptance, the SAT itself is posing a burden to students' access to college. Instead of focusing on increasing participation rates, the SAT shows focus more test preparation resources.  

Citations
<br>
1: https://www.collegeboard.org/releases/2018/more-than-2-million-students-in-class-of-2018-took-sat-highest-ever
<br>
2: https://www.edweek.org/ew/articles/2018/10/31/sat-scores-rise-as-number-of-test-takers.html
<br>
3: https://www.washingtonpost.com/education/2018/10/23/sat-reclaims-title-most-widely-used-college-admission-test/?utm_term=.c1ca18b8b596

---
## Conclusions & Recommendations 
I found that the College Board is focusing on increasing participation rates while not focusing on the outcome of test scores. There is a significant negative correlation between participation rates and test scores, which means that the higher the participation rates, the lower the test scores (and vice versa). Focusing solely on increasing participation rates by the College Board is equivalent to the College Board assisting in  deterioration of test scores. This may help in achieving an ideal of a 100% participation rate, however, a majority of US high schoolers will perform very poorly on the test.
<br>
**Recommendations**
<br>
Therefore in order to achieve sustainable growth and be a resource trusted by students nationwide (i.e., its primary customers), I recommend the following:  
- Instead of keeping focus only on the participation rate, they must have to focus seriously towards improving access to test preparation resources. 
- Create a better test preparation support for states with highest participation rates, particularly in the East Coast where there is a concentration of states with high performance and low test scores.

--- 
## Data Sources
The sources of the datasets used in this analysis: 
- [SAT 2017 dataset](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/)
- [SAT 2018 dataset](https://reports.collegeboard.org/sat-suite-program-results/state-results)


