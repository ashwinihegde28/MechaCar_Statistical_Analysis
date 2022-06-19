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

### Deliverable 1 - Linear Regression
The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. Using the knowledge of R, designed a linear model that predicts the mpg of MechaCar prototypes by using several variables from the MechaCar_mpg.csv file. <br>
![Capture 1](https://github.com/ashwinihegde28/MechaCar_Statistical_Analysis/blob/main/images/Capture1.PNG) <br>

####  Summary of Linear Regression model
A summary of the linear regression can be displayed to determine the quality of the dataset.  In this distribution of the residuals, the dataset fits in with the normal parameters, where the absolute value of the min and max are comparable |-19.47|~|18.58| and the median -.07 is close to zero.
1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?       
  * 95% level of confidence was predetermined, meaning the p-value should be compared to alpha = .05 level of significance to verify if statistically significant.In summary, vehicle length and ground clearance variables represent non-random amounts of variance as applied to the mpg values. 

2. Is the slope of the linear model considered to be zero? Why or why not? 
  * The p-Value 5.35e-11 is much smaller than the assumed significance level of 0.05,Therefore, the null hypothesis cannot be accepted, indicating that the slope of this linear model is not zero.

3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not
  * The r-squared value of the linear model is 0.7149, which means that it will determine approximately 71% of all mpg predictions. MechaCar prototypes are predicted to achieve good mpg by different regression models.
 
### Deliverable 2 - Summary Statistics on Suspension Coils
#### Manufacturing Lot Summary
Below is the summary statistics of all of the manufacturing lots.  The mean is 1498.78 for this sample and the population mean was determined to be 1500. <br> 
![Capture 2.1](https://github.com/ashwinihegde28/MechaCar_Statistical_Analysis/blob/main/images/Capture2.1.PNG) <br>
#### Summary by Manufacturing Lot Number
The means of the lot numbers are similar to the population mean and the sample mean.<br>
![Capture 2.2](https://github.com/ashwinihegde28/MechaCar_Statistical_Analysis/blob/main/images/Capture2.2.PNG) <br>
1. The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?    
- The variance for the total manufacturing lot is 62 < 100, which is within the expected design specifications of staying under 100 PSI.  However, when reviewing the data by Lot number, Lot 3 is a large contributing factor to the variance being high.  Lot 3 shows a variance of 170 > 100 which does not meet the design specifications.  Lot 1 and Lot 2 have significantly lower variance, 1 and 7 respectively. 

### Deliverable 3 - T-Tests on Suspension Coils
1. The t test result on all the lots is as follows. Since the p-value of three lots is more than our significance value of 0.05, we FAIL to reject the NULL hypothesis for all manufacturing lots grouped together. <br>
![Capture 3.1](https://github.com/ashwinihegde28/MechaCar_Statistical_Analysis/blob/main/images/Capture3.1.PNG) <br>

2. Lot 1, The p-value for lot 1 is 1 above the significance level, assuming our significance level is 0.05 percent. As a result, the null hypothesis cannot be rejected, and therefore, they are equivalent. <br>
![Capture 3.2](https://github.com/ashwinihegde28/MechaCar_Statistical_Analysis/blob/main/images/Capture3.2.PNG) <br>

3. Lot 2: The p-Value is less than 0.05, which is statistically significant. It indicates strong evidence against the null hypothesis. The mean falls within the 95% confidence interval. <br>
![Capture 3.3](https://github.com/ashwinihegde28/MechaCar_Statistical_Analysis/blob/main/images/Capture3.3.PNG) <br>

4. Lot 3: p-value greater than .05, which means the null hypothesis cannot be rejected. However, the mean falls within the 95% confidence interval.<br>
![Capture 3.4](https://github.com/ashwinihegde28/MechaCar_Statistical_Analysis/blob/main/images/Capture3.4.PNG) <br>
  
### Study Design: MechaCar vs Competition
  Using the knowledge of R, designed a statistical study to compare the performance of the MechaCar vehicles against the performance of vehicles from other manufacturers. A statistical study has been designed to determine the performance of MechaCar vehicles in comparison with those produced by other manufacturers. Potential metrics that consumers could find interesting in this study might include cost, city or highway fuel efficiency, horsepower, maintenance cost, or safety rating.
1. What metric or metrics are you going to test?
The next metrics to test should be the safety rating, horsepower, and highway fuel efficiency, which address some safety concerns of consumers.
2. What is the null hypothesis or alternative hypothesis?
 - Null Hypothesis : MecharCar and Competition vehicles perform similarly in terms of average city and highway fuel efficiency. 
 - Alternative Hypothesis : Competition vehicles and MecharCars have different average city or highway fuel efficiency.
3. What statistical test would you use to test the hypothesis? And why?.
 - Using a multiple linear regression statistical summary would show how the variables impact the safety ratings for MechaCar and their competitors.
4. What data is needed to run the statistical test? 
 - A random sample of n > 30 for MechaCar and their competitor, would need to be collected including the safety ratings, highway fuel efficiency, and horsepower plus running the data through RStudio.
