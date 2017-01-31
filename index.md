---
title       : Data Quality and Data Types
subtitle    : Data based decision making course
author      : Daniel Anderson
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : zenburn      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
--- 
<style>
em {
  font-style: italic
}
</style>

<style>
strong {
  font-weight: bold;
}
</style>



## ... Where were we? 

* Data types and distributions
* Outcome versus predictor variables
* Observational versus experimental data


----
## Remember

* Get R installed: https://cran.r-project.org
* Get RStudio installed: https://www.rstudio.com/products/rstudio/download/

**NOTE:** If you need help with either of the above, please contact me. I'd like everybody to be ready to go **before** we need to use it. Best to get it installed now and make sure it's working so we can troubleshoot if not.

----
## First off..

Just because data exist, doesn't mean they are meaningful

![plot of chunk plot_no_bar](assets/fig/plot_no_bar-1.png)

----
![plot of chunk plot_bar](assets/fig/plot_bar-1.png)

----
## Another example



![plot of chunk plot1](assets/fig/plot1-1.png)

----
## "Stacked" groups

![plot of chunk plot2](assets/fig/plot2-1.png)

----
## Take home message
Know your data, understand where they came from, and the questions they can and cannot address.

---- .segue
# Data types and distributions

---
## Data types
Two basic types of data: Categorical and Numerical
>* Categorical: Variable can only take on discrete values
	* Two types of categorical variables
		+ Ordered (ordinal)
			- small, medium, large
			- strongly disagree, diagree, agree, strongly agree
		+ Nominal
			- red, green, yellow, blue, purple
			- Teacher 1, Teacher 2, ..., Teacher *n*
>* Quantitative or Continuous: Variable can take on any real number
	* Technically quantitative/continuous variables have either *interval* or *ratio* properties, but we won't worry about that too much.

----
## Discussion
Talk with a neighbor. Identify what types of data each of the following are. Distinguish between ordinal and nominal categorical data.

* State test scores
* State test performance level classifications
* Number of office referrals
* Disability status
* Grades
* Grade point average
* Course placement
* Free and reduced price lunch eligibility

----
## Thinking deeper about data
* Imagine data from state test scores for all students in a school
* Now image data from the number of office discipline referrals for every student in the school.

<br>
Discuss with your neighbor - how would these data look different? How would they be similar?

----- &twocol
## Data distributions

*** =left

# Normally distributed data
![plot of chunk norm_dist](assets/fig/norm_dist-1.png)

*** =right
# Count distributions (Poisson)

![plot of chunk r_poiss](assets/fig/r_poiss-1.png)

----
## Why does this matter?
>* Whether you realize it or not, you're always making assumptions about your data.
>* The distribution corresponds to the probability that a particular value will occur.
>* If you make incorrect assumptions about your data, you're likely to arrive upon incorrect conclusions.

---
## What about categorical data?
* Generally, data with two categories (head/tails) are assumed to follow the *binomial* distribution. 
* Probability of an event does not have to be 0.5

<br> 

## More than two categories?
* Multinomial distribution
* Similar to the binomial but with more categories, and each category has an assigned probability. 

----
## Binomial Distribution

Let's play!

http://shiny.albany.edu/stat/binomial/


----
## General recommendations
* Don't categorize continuous data (throwing away information).
* Look at your data first! 
* Consider all possible observations for the variable. Were all observed?
* Make sure you understand your data before you start to make decisions or form conclusions from it.

---- .segue
# Predictors versus outcomes

----
## Outcome variable
* Also called the **dependent variable (DV)**. 
* The thing you're interested in. 
* What do you want to predict? Improve? Change?

<br>

**Examples:** State test scores, office referrals, peer-to-peer interactions, use of evidence-based practices, etc.

----
## Predictor variable
* Also called the **independent variable (IV)**.
* The DV is expected to change as a function of the IV(s).
* In experimental designs, the IV is manipulated (receive/do not receive treatment).

<br>

**Examples:** Treatment status, ELL-status, Disability status, etc.

----
## Predictors versus control variables
* Sometimes you want to include variables that are not directly related to your research question, so you can **control** (statistically) for their impact.
* Statistical controls are never as strong as design controls (and don't let anyone try to convince you otherwise).

<br>

**Examples:** Gender, race/ethnicity, FRL-status, Prior achievement, etc.

----
## Sometimes it gets fuzzy
* What is the relationship between reading and math state test scores?

<br> 

Try to be clear when you're communicating with others. If the question solely focuses on relationships, that's fine, but otherwise try to be more clear.

>* How do reading scores predict math scores?

----
## Discussion
* Can the same variable be both a predictor and outcome variable in **different** studies?
* Can the same variable be both a predictor and outcome variable in **the same** study?
* Can the same variable be both an independent variable and a control variable in the same study?

----
## Challenge

For each question below, identify the IV and the DV, and describe each variable as nominal, ordinal, or continuous.

1. To what extent does students' Grade 3 state test score in reading predict whether the student will graduate from high school?
2. How do students differ in math state test score gains from Grades 3 to 4, based on the classroom they were enrolled in at Grade 3? 
3. How do students' scores on a fall fluency measure predict their state test score in the spring?
4. To what extent does free and reduced price lunch eligibility status predict enrollment in special education? 


-----
## Thinking about questions
Brainstorm with your neighbor: Come up with an example research question for each of the following scenarios. 

<br>

* Categorical predictor, categorical outcome
* Categorical predictor, continuous outcome
* Continuous predictor, categorical outcome
* Continuous predictor, continuous outcome

---- .segue
# Observational versus experimental data

----
## Most data are non-experimental
* Experimental data are collected within a specific research design.
* Experimental data include:
	+ Manipulation of the IV
	+ Random assignment to treatment
* All other data are non-experimental

Besides the above characteristics, what distinguishes experimental data from non-experimental data? 

<br>
Are experimental data more or less important than non-experimental data?

----
## Experimental versus non-experimental data
* Experimental data are collected to try to determine the *casual* effect of a treatment.
* Non-experimental data are essentially always threatened by the omitted variable bias (causal attribution tenuous at best)

----
## Spurious correlations

http://www.tylervigen.com/spurious-correlations

>* Note, these all have dual axes, which is a really bad ideal (see http://stackoverflow.com/questions/3099219/plot-with-2-y-axes-one-y-axis-on-the-left-and-another-y-axis-on-the-right)

>* Well-implemented experiments eliminate the possibility of spurious correlations


----
## What we still didn't get to...
* Samples and populations (and sampling methods)


---- 
## Next time
# Data visualization dos and don'ts


