# MechaCar Statistical Analysis
Module 15: Statistics and R

# Overview
AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called the data analytics team to review the production data for insights that may help the manufacturing team.


# Resources
* Data Source: various csv files
* Language:
  - R

* Development tools: 
  - Visual Code 1.62.3
  - R Studio 2022.02.0



# Deliverables
## Deliverable #1
Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes

![Deliverable #1](/Resources/Deliverable1.png)

### Question #1:
*Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?*

After reviewing the summary found that the `Pr(>|t|)` value for the  __vehicle_length__ and __ground_clearance__, as well as the __intercept__ shows they're are unlikely to provide random amount of variance withing the linear model, so they have a significant impact on the __mpg__.

### Question #2:
*Is the slope of the linear model considered to be zero? Why or why not?*

__No__, according to the `Pr(>|t|)` value the __intercept__ indicates a significant amount of variability.

### Question #3:
*Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?*

__Yes__, `R-squared` is __0.7149__ indicating a strong correlation.



## Deliverable #2

Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots

![Total Summary Table](/Resources/total_summary.png)

An overall __62.29__ `Variance` indicates the suspension coils meet the design specification which requires it should not exceed 100 PSIs.

![Lot Summary Table](/Resources/lot_summary.png)

By grouping by __Manufacturing_lot__ I found that __Lot 1__ and __Lot 2__ both meet the design specifications but the `Variance` for __Lot 3__ was of __170.26__ which is not in compliance.

## Deliverable #3

Run t-tests to determine if the manufacturing lots are statistically different from the mean population

![Overall t-tes](/Resources/t-test1.png)

Assuming a level of significance of __0.05__, with a NULL Hypothesis of `mu = 1500` we found that with a `p-value` of __0.6028__ we fail to reject it.

![t-test by Lot](/Resources/t-testByLot.png)

After reviewing individual t-test results (by Manufacturing Lot), I've found the following:
* __Lot 1__ and __Lot 2__ are __NOT significanlty__ different from the population with a `p-value` of __1__ and __0.0672__ respectevively.
*  __Lot 3__ __*IS significanlty*__ different from the population with a `p-value` of __0.04168__.


## Deliverable #4

Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

I've to start by saying I'm not a car fan, therefore, I would require a knowledgeable person's opinion on this subject, but I'll use a wild guess.

- __Metric__: Number of cylinders
- __Hypothesis__
    * *NULL*: There is no difference between MechaCar cars and other manufacturers cars.
    * *Alternate*: There is a difference
- __Statistical Test__: `Multiple Linear Regresion` including __mpg__ and the __No of cylinders__.
- __Data__: MechaCar and other manufacturers car's definition, including, all data provided for the MechaCar cars plus # of cylinders.


