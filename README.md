# MechaCar_Statistical_Analysis
MechaCar_Statistical_Analysis using R and Statistics

## Project Overview


* Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes.
* Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots.
* Run t-tests to determine if the manufacturing lots are statistically different from the mean population.
* Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.
* Project useses RStudio and dplyr library.


### Steps Involved:
1. Load, clean up, and reshape datasets using tidyverse in R.
2. Visualize datasets with basic plots such as line, bar, and scatter plots using ggplot2.
3. Generate and interpret more complex plots such as boxplots and heatmaps using ggplot2.
4. Plot and identify distribution characteristics of a given dataset.
5. Formulate null and alternative hypothesis tests for a given data problem.
6. Implement and evaluate simple linear regression and multiple linear regression models for a given dataset.
7. Implement and evaluate the one-sample t-Tests, two-sample t-Tests, and analysis of variance (ANOVA) models for a given dataset.
8. Implement and evaluate a chi-squared test for a given dataset.
9. Identify key characteristics of A/B and A/A testing.
10. Determine the most appropriate statistical test for a given hypothesis and dataset.

### Deliverable 1
### Linear Regression
The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. Using my knowledge of R, designed a linear model that predicts the mpg of MechaCar prototypes by using several variables from the MechaCar_mpg.csv file. Then, write a short interpretation of the multiple linear regression results.<br>
![Capture 1](https://github.com/ashwinihegde28/MechaCar_Statistical_Analysis/blob/main/images/Capture1.PNG) <br>

####  Summary of Linear Regression model
A summary of the linear regression can be displayed to determine the quality of the dataset.  In this distribution of the residuals, the dataset fits in with the normal parameters, where the absolute value of the min and max are comparable |-19.47|~|18.58| and the median -.07 is close to zero.
1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?       
  * 95% level of confidence was predetermined, meaning the p-value should be compared to alpha = .05 level of significance to verify if statistically significant.In summary, vehicle length and ground clearance variables represent non-random amounts of variance as applied to the mpg values. 

2. Is the slope of the linear model considered to be zero? Why or why not? 
  * The p-Value 5.35e-11 is much smaller than the assumed significance level of 0.05,Therefore, the null hypothesis cannot be accepted, indicating that the slope of this linear model is not zero.

3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not
  * The r-squared value of the linear model is 0.7149, which means that it will determine approximately 71% of all mpg predictions. MechaCar prototypes are predicted to achieve good mpg by different regression models.
 
### Deliverable 2
### Summary Statistics on Suspension Coils
#### Manufacturing Lot Summary
Below is the summary statistics of all of the manufacturing lots.  The mean is 1498.78 for this sample and the population mean was determined to be 1500. <br> 
![Capture 2.1](https://github.com/ashwinihegde28/MechaCar_Statistical_Analysis/blob/main/images/Capture2.1.PNG) <br>
#### Summary by Manufacturing Lot Number
The means of the lot numbers are similar to the population mean and the sample mean.<br>
![Capture 2.2](https://github.com/ashwinihegde28/MechaCar_Statistical_Analysis/blob/main/images/Capture2.2.PNG) <br>
1. The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?    
- The variance for the total manufacturing lot is 62 < 100, which is within the expected design specifications of staying under 100 PSI.  However, when reviewing the data by Lot number, Lot 3 is a large contributing factor to the variance being high.  Lot 3 shows a variance of 170 > 100 which does not meet the design specifications.  Lot 1 and Lot 2 have significantly lower variance, 1 and 7 respectively. 
  
