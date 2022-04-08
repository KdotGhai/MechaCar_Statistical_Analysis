# MechaCar_Statistical_Analysis
Module 15
<br> 
## Project Overview
&nbsp;&nbsp;&nbsp;&nbsp;The goal of the project is to analyze metrics that can affect the manufacturing a new car prototype and compare vehicle performance across different manufacturer lots. These metrics include vehicle length, weight, spoiler angle, ground clearance, AWD capabilities, MPG, and PSI.

## Linear Regression to Predict MPG
![Linear Regression](https://github.com/KdotGhai/MechaCar_Statistical_Analysis/blob/30f73892373d438e1f8e2941c84b519c30d3ab7a/Images/linear_regression.PNG)

3 Key Takeaways:
* Variance of a non-random variable is usually 0. Given this fact, the intercept, vehicle_length, and ground_clearance coeeficients can be said to provide a non-random amount of variance to the mpg values. 
* At a significance level of 0.05(0.025 at each tail end) for 95% confidence level, we are able to reject the null hypothesis because of the extremely small p-value(5.35e-11). The null hypothesis of a linear regression states that the slope is equal to 0. However, if we reject the null hypthesis, we're stating that alternative hypothesis (slope ≠ 0) is true, we must take into consideration in select scenarios where the p-value still falls under the rejection area but may be too high a value to consider rejecting the null hypothesis.
* Multiple R-squared increases as more variables are passed through the regression. However, adjusted R-squared controls against this increase, and adds penalties for the number of predictors in the model, thus making it a more accurate predictor of how effective the linear model is. An adjusted R-square of 0.6825 concludes that this linear model suggest moderately postive correlations with all the independent varaibles.
<br>

## Summary Statistics on Suspension Coils
<p align="center">
<img src = "https://github.com/KdotGhai/MechaCar_Statistical_Analysis/blob/30f73892373d438e1f8e2941c84b519c30d3ab7a/Images/lot_summary_table.PNG" width="700" height="200"/>
<img src = "https://github.com/KdotGhai/MechaCar_Statistical_Analysis/blob/30f73892373d438e1f8e2941c84b519c30d3ab7a/Images/total_summary_table.PNG" width="700" height="170"/>
</p>

&nbsp;&nbsp;&nbsp;&nbsp;The overall variance for the entire dataset indicates that the current manufacturing data meets the 100 pounds per square inch variance limitation. However, when separated into three lots, the third lot demonstrates higher variance, the lots are chosen randomly so there is high probability of it not meeting the necessary suspension coils requirement.
  
## T-Test on Suspension Coils
### T-Test on Entire Lot
<p align="center">
<img src="https://github.com/KdotGhai/MechaCar_Statistical_Analysis/blob/724893607de835ab56e57abe287bb995b57a822a/Images/t-test.PNG">
</p>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;At a significance level of 0.05, we fail to reject the null hypothesis since the p-value equals 0.06. Therefore, we cannot reject the fact that the sample mean may be equivalent to the true population mean or that no significant difference exists.
