# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

#

### GA Project 1

### Table of content
 - Problem Statement
- Data Dictonaries
- Data analysis
- Conclusions
### Problem Statement

### Who we are?
a group of data scientist that works with board of dicrectors from College Board in California

### The real problem
we realised that the low income cycle cause by the wide income gap in certain states. whcih ultimately lead us to have an observation at the SAT participation rate.

Not only poor family income group are unable to break free from this cycle , their children are unable as well. thus the cycle continues.

Hence, Education is essential factor that can lead ones life out of poverty.
Therefore...

This studies is on relationship of SAT participation rate vs Median household income.
---

### Datasets data 2017 to 2019
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*string*|2017 SAT Scores by State|States in the USA
|**participation_2017**|*float*|2017 SAT Scores by State|Participation rates for SAT in 2017 by state
|**ebrw_2017**|*float*|2017 SAT Scores by State|Average SAT Evidence-based Reading and Writing Score in 2017 by state
|**math_2017**|*float*|2017 SAT Scores by State|Average SAT Mathematics Score in 2017 by state
|**total_2017**|*float*|2017 SAT Scores by State|Average SAT Total Score in 2017 by state, where Total = Math + EBRW
|**participation_2018**|*float*|2018 SAT Scores by State|Participation rates for SAT in 2018 by state
|**ebrw_2018**|*float*|2018 SAT Scores by State|Average SAT Evidence-based Reading and Writing Score in 2018 by state
|**math_2018**|*float*|2018 SAT Scores by State|Average SAT Mathematics Score in 2018 by state
|**total_2018**|*float*|2018 SAT Scores by State|Average SAT Total Score in 2018 by state, where Total = Math + EBRW
**participation_2019**|*float*|2019 SAT Scores by State|Participation rates for SAT in 2019 by state
|**ebrw_2019**|*float*|2019 SAT Scores by State|Average SAT Evidence-based Reading and Writing Score in 2019 by state
|**math_2019**|*float*|2019 SAT Scores by State|Average SAT Mathematics Score in 2019 by state
|**total_2019**|*float*|2019 SAT Scores by State|Average SAT Total Score in 2019 by state, where Total = Math + EBRW

#### Provided Data

* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State ([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))
* [`sat_2019_ca.csv`](./data/sat_2019_ca.csv): 2019 SAT Scores in California by School

#### Additional Data
* [`household_income_county.csv`](./data/household_income_county.csv): Median Household income data
([source](https://www.census.gov/search-results.html?q=california+median+income&page=1&stateGeo=none&searchtype=web&cssp=SERP&_charset_=UTF-8))

---
### Data Analysis
![image.png](https://i.postimg.cc/Z5bsQCFv/demo1.png)
![image.png](https://i.postimg.cc/XYs164QH/demo2.png)
---

### Conclusions & recommendations
Based on the data, SAT participation rates are largely influenced by the Median Household income . Participation rate is tied plays a low part in low income families. Not to mention, even after the students are able to take SAT entries, they will still have to fare for the University load, which would be a burden that may stick with them even after 5 years. Hence, to solve our problem statement we have recommendations.

Some recommendations:
 - Offering SAT at no cost
- Conducting SAT exam during regular school hours with transportation provided.
- Engagement with the school counselor
- Free access to the College Board's official SAT online course

---
