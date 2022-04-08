# MechaCar_Statistical_Analysis
Module 15
<br> 
## Project Overview
&nbsp;&nbsp;&nbsp;&nbsp;The goal of the project is to analyze metrics that can affect the manufacturing a new car prototype and compare vehicle performance across different manufacturer lots. These metrics include vehicle length, weight, spoiler angle, ground clearance, AWD capabilities, MPG, and PSI.

## Linear Regression to Predict MPG
![Linear Regression](https://github.com/KdotGhai/MechaCar_Statistical_Analysis/blob/30f73892373d438e1f8e2941c84b519c30d3ab7a/Images/linear_regression.PNG)
<br>
![Linear Regression Summary](https://github.com/KdotGhai/MechaCar_Statistical_Analysis/blob/5b33a9a6efc1875b7eb1ec39cc8be621ffda139c/Images/linear_regression_summary.PNG)

3 Key Takeaways:
* Variance of a non-random variable is usually 0. Given this fact, the intercept, vehicle_length, and ground_clearance coeeficients can be said to provide a non-random amount of variance to the mpg values. 
* At a ```significance level of 0.05(0.025 at each tail end) for 95% confidence level```, we are able to reject the null hypothesis because of the extremely small ```p-value(5.35e-11).``` The null hypothesis of a linear regression states that the ```slope is equal to 0```. However, if we reject the null hypthesis, we're stating that alternative hypothesis ```(slope ≠ 0)``` is true, we must take into consideration in select scenarios where the p-value still falls under the rejection area but may be too high a value to consider rejecting the null hypothesis.
* Multiple R-squared increases as more variables are passed through the regression. However, adjusted R-squared controls against this increase, and adds penalties for the number of predictors in the model, thus making it a more accurate predictor of how effective the linear model is. An adjusted ```R-square of 0.6825``` concludes that this linear model suggest moderately postive correlations with all the independent varaibles.
<br>

## Summary Statistics on Suspension Coils
<p align="center">
  <br>  <b> LOT SUMMARY</b>  </br>
<img src = "https://github.com/KdotGhai/MechaCar_Statistical_Analysis/blob/30f73892373d438e1f8e2941c84b519c30d3ab7a/Images/lot_summary_table.PNG" width="700" height="200"/>
<br>
  <br>  <b> TOTAL SUMMARY TABLE</b>  </br>
<img src = "https://github.com/KdotGhai/MechaCar_Statistical_Analysis/blob/30f73892373d438e1f8e2941c84b519c30d3ab7a/Images/total_summary_table.PNG" width="700" height="170"/>
</p>

&nbsp;&nbsp;&nbsp;&nbsp;The overall variance for the entire dataset indicates that the current manufacturing data meets the 100 pounds per square inch variance limitation. However, when separated into three lots, the third lot demonstrates higher variance, the lots are chosen randomly so there is high probability of it not meeting the necessary suspension coils requirement.
  
## T-Test on Suspension Coils
### T-Test on Entire Lot
<p align="center">
<img src="https://github.com/KdotGhai/MechaCar_Statistical_Analysis/blob/724893607de835ab56e57abe287bb995b57a822a/Images/t-test.PNG">
</p>
<br>

&nbsp;&nbsp;&nbsp;&nbsp; At a ```significance level of 0.05,``` we fail to reject the null hypothesis since the```p-value equals 0.06```. Therefore, we cannot reject the fact that the sample mean may be equivalent to the true population mean or that no significant difference exists.

## T-Test on Three Smaller Lots
<p align="center">
<img src="https://github.com/caseychen3605/MechaCar_Statistical_Analysis/blob/main/Resources/lots_t_test.PNG">
</p>

#### Lot 1

At a ```significance level of 0.05```, we fail to reject the null hypothesis since the p-value equals 1. An interesting correlation between p-value and confidence intervals is that as the p-values get larger, the confidence interval becomes smaller, implying more precision in predicting the true population mean.

#### Lot 2
At a ```significance level of 0.05```, we fail to reject the null hypthesis again since the ```p-value equals 0.6072.``` The second lot also has a relatively small confidence interval.

#### Lot 3
At a ```significance level of 0.05```, we can reject the null hypothesis since the ```p-value equals 0.04168.``` The mean of this sample is also significantly smaller in comparison to the previous two lots. More importantly, unlike the previous two lots, the confidence interval for the third lot does not include the predicted population mean.


## Study Design: MechaCar vs. Competition
This study would involve collecting data on MechaCar and its comparable models across several different manufacturers over the last 3 years.

* What are the competitions' comparable models(general-consumer/family cars), 
* Which car brands will MechaCar be competing with head-to-head? which cars types will be included in the study?
* Which directly relevant factors will we look at to determine selling price?
 

#### Metrics
Collecting data for comparable models across all major manufacturers for past 4 years for the following metrics:

*  Safety Feature Rating: **Independent Variable**
*  Malfunctions/recalls: **Independent Variable**
*  Current Price (Selling): **Dependent Variable**
*  Engine (Electric, Hybrid, Gasoline / Conventional): **Independent Variable**
*  Average Annual Cost of ownership (Maintenance): **Dependent Variable**
*  MPG (Gasoline Efficiency): **Independent Variable**
*  Consumer Ratings/Usage(such as: Work, Personal, Family, Mixed):**Dependent Variable**


#### Hypothesis: Null and Alternative
After determining which factors are key for the MechaCar's genre:

 * Null Hypothesis: MechaCar is fairly priced based on its performance of key factors for its genre.
 * Alternative Hypothesis: MechaCar is NOT priced correctly based on performance of key factors for its genre.
 
#### Statistical Tests
A **multiple linear regression** would be used to determine the factors that have the highest correlation/predictability with the list selling price (dependent variable); which combination has the greatest impact on price (it may be all of them!). We may also need to consider doing a paired t-test mainly on MPG and Maintenance to determine their impact over the period of time or at various points within the 4 years worth of data

<br>

## Sources of info:
* The Organic Chemistry Tutor
  - Basic Fundamentals of types of tests: https://youtu.be/XHPIEp-3yC0
  - Z-test example and basic explanation: https://youtu.be/zJ8e_wAWUzE
  - P-Value Method: https://youtu.be/8Aw45HN5lnA
* Free Online In-Depth stat book: https://onlinestatbook.com/2/estimation/mean.html
* R Squared vs Adjusted R Squared: https://stats.stackexchange.com/questions/353807/which-is-better-r-squared-or-adjusted-r-squared
* Basics of R Squared: https://www.investopedia.com/ask/answers/012615/whats-difference-between-rsquared-and-adjusted-rsquared.asp#:~:text=Many%20investors%20prefer%20adjusted%20R,the%20stock%20index%20is%20measured.
* Interpreting R Squared: https://www.investopedia.com/terms/r/r-squared.asp#:~:text=In%20other%20fields%2C%20the%20standards,would%20show%20a%20low%20correlation.
