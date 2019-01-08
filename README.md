# Project 1: SAT & ACT Analysis

## Problem Statement: 
More than three million students take either the SAT or the ACT each year. What insights can we gain from the participation rates and scores for each test?

## Executive Summary
Key findings:
1. Correcting for states with low participation yields an approximately normal distribution suitable for conducting inferential statistics.
2. Average scores negatively correlated with participation rates
3. States with large changes in participation rates tended to score lower on average


### Contents:
- [2017 Data Import and Cleaning](#2017-Data-Import-and-Cleaning)
- [2018 Data Import and Cleaning](#2018-Data-Import-and-Cleaning)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Data Visualization](#Visualizing-the-data)
- [Descriptive and Inferential Statistics](#Descriptive-and-Inferential-Statistics)
- [Outside Research](#Outside-Research)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)

### Data Sources:
- [2017 SAT Data](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/)
- [2017 ACT Data](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows)
- [2018 SAT and ACT Data](http://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf)

#### Data dictionary 
Quick overview of features/variables/columns, alongside data types and descriptions:

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|SAT and ACT|The state from which the data was gathered.|
|2017_sat_participation|float64|SAT|Participation rate for the 2017 SAT|
|2017_sat_reading|float64|SAT|Average Evidence-Based Reading and Writing score for the 2017 SAT|
|2017_sat_math|float64|SAT|Average Math score for the 2017 SAT|
|2017_sat_total|float64|SAT|Average Total score for the 2017 SAT (Sum of Reading and Math)|
|2017_act_participation|float64|ACT|Participation rate for the 2017 ACT|
|2017_act_english|float64|ACT|Average English score for the 2017 ACT|
|2017_act_math|float64|ACT|Average Math score for the 2017 ACT|
|2017_act_reading|float64|ACT|Average Reading score for the 2017 ACT|
|2017_act_science|float64|ACT|Average Science score for the 2017 ACT|
|2017_act_total|float64|ACT|Composite score for the 2017 ACT (Average of English, Math, Reading and Science)|

### Additional data of interest:
#### Colorado
Colorado initiated bidding for mandatory statewide college admission testing in 2015, and settled on the SAT, causing a steep drop in 2018 ACT participation.
> Source: [Colorado Department of Education](https://www.cde.state.co.us/assessment/coloradosat)

#### Illinois
Illinois mandated SAT participation across the state for High School Juniors in 2017. This caused SAT participation to jump to 100% and had a corresponding negative impact on the state's overall average SAT scores.
> Source : [Chicago Tribune](https://www.chicagotribune.com/news/ct-illinois-chooses-sat-met-20160211-story.html)

#### Nevada
Nevada averages lowest in 2017 ACT scores among all states with high participation. Nevada made it mandatory for all 11th grade students to take the ACT in 2016, which education officials have blamed for the drop in average scores. It is thought that this drop may be the result of forcing students with no college ambitions, who will likely not take the test seriously, to participate.
> Source: [The Nevada Independent](https://thenevadaindependent.com/article/nevadas-act-scores-rank-dead-last-calling-into-question-students-college-readiness)

## Conclusions and Recommendations
- To conduct inferential statistics we need to exclude outlier states with low participation rates.
- States with low participation tend to score higher.
>This is likely the result of selection bias, as more motivated, better prepared students are more likely to take the test if participation is not mandated by the state.

- Large shifts in participation rate can negatively impact scores.
- The trend in participation rates from 2017 to 2018 favors the SAT over the ACT.