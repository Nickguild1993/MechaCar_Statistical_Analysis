# MechaCar Statistical Analysis

### Deliverable 1

## Linear Regression to Predict MPG

Below is an image of the linear regression that shows **vehicle length**, **ground clearance** as well as the **intercept value (MPG)** having statistical significance. 

![Alt_img](https://github.com/Nickguild1993/MechaCar_Statistical_Analysis/blob/main/images/Mod_15_Deliv_1_regression.png)

Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

- MPG (which of course, is the intercept), vehicle length, along wtih ground clearance are the variables that provided a non-random amount of variance to predicting the MPG values. 

Is the slope of the linear model considered to be zero? Why or why not?

- No, the slope of the linear model is not zero.  This is because our p-value is  < alpha level of 0.05 meaning that we reject the null hypothesis that the slope of the linear model is zero.

Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

- To a degree, but overall no, I'm afraid not.  While the multiple R-squared value is .7149, which means that the linear model is able to correctly predict the MPG value of a car in *this* dataset 71% of the time based on the selected variables, the intercept is statistically significant, which means that there are outstanding variables that are contributing to the variation in our model.  This is an issue because we ran all of our available variables in our multiple linear model, so we have nothing further that we can try testing on to explain what hidden/outstanding variable(s) are influencing MPG values.  Without that information, I would not be comfortable saying that the model we created can predict MPG values for cars in this dataset, and it definitely doesn't seem to have a solid level of external validity, given that we only have two variables that are returning as statistically significant.

### Deliverable 2

## Summary Statistics on suspension coils


Below are the summary statistics results grouped by their respective Lot.

![Alt_Image](https://github.com/Nickguild1993/MechaCar_Statistical_Analysis/blob/main/images/Mod_15_Deliv_2_grouped_summary.png)

- The current manufacturing data shows that unfortunately, the requirement that the variance of the suspension not exceed 100 pounds per square inch (PSI) is not being observed by the brain genuises in Lot 3.  As the summary above shows, they currently have a variance of 170.28 PSI, which not only exceeds the prescribed maximum by more than 70 PSI, but it's also way out of line with the variance that we're observing in Lot 1 (variance of .97 PSI) and 2 (variance of 7.49 PSI).  Those two lots' variance levels for suspension PSI are but a fraction of Lot 3's levels.  At least then, the sky-high PSI variance being observed in the suspension coils coming out of Lot 3 is an isolated issue to that specific lot. 

### Deliverable 3

## T-Tests on Suspension Coils

Hº : There is no significant statistical difference between the observed sample mean PSI and the population mean PSI.

H1 : There is a significant statistical difference between the observed sample mean PSI and the population mean PSI.

When we ran the one sample t-test across **all observations**, we returned a p value of .060 which is greater than our alpha of 0.05. Therefore, we fail to reject the null hypothesis, meaning that there is no statistical difference between the observed sample mean PSI across all observations and the population mean PSI.

### Subset testing results 

Running the one-sample t-test while using the subset argument for "Lot1" we returned a p value of 1.00, which again means we fail to reject the null hypothesis as this p value > alpha level of 0.05.

For the "Lot2" subset one-sample t-test, we returned a p value of 0.6072, which again dictates that we fail to reject the null hypothesis as the p value > alpha level of 0.05.

![Alt_Image](https://github.com/Nickguild1993/MechaCar_Statistical_Analysis/blob/main/images/Mod_15_Lot3test.png)

Above is the statistical summary for the "Lot 3" subset.  This was the only subset that showed a significiant difference from the population mean PSI.

For the "Lot3" subset one-sample t-test, we returned a p value of 0.0416, which is less than our alpha level of 0.05!  Therefore, we reject the null hypothesis and accept the alternate hypothesis which states that there is a significant statistical difference between the observed sample mean (Lot 3) PSI and the population mean PSI. 

### Deliverable 4

## Study Design: MechaCar vs ALL TAKERS

In order to quantify how MechaCar performs against similar vehicles I would run a series of one-sample t-tests in which the population is an average (on various metrics) of similiar cars from across the industry.  The reason for choosing a one sample t-test is because it allows me to compare my specific car(s), on any metric I choose, to an average of every other type of car in that same class. With that information, I'll be able to readily see which metrics the MechaCar is statistically different from its competition, and leverage those facets into an integrated marketing campaign highlighting things like how "the MechaCar is quantifiably safer than every other sedan in its class" or "The MechaCar retains its value at a higher rate over time better than any other sedan in its class".  

For metrics, I would look to test the following: **MPG, Safety Rating, Initial Cost, Resale Value**, and **Emission Rating**.  Using the one sample t-test, I would determine if the sample (MechaCar) mean for "x" metric has a significant statistical difference from the population (comparable cars) mean.

Hypothesis Testing:

I will be utilzing an alpha level = 0.05

Null Hypothesis: There is no significant statistical difference at an alpha level of 0.05 between the MechaCar mean [MPG, Safety Rating, Initial Cost, Resale Value, Emission Rating] and the population mean [metric].

Alternative Hypothesis: There is a significant statistical difference at an alpha level of 0.05 between the MechaCar mean [MPG, Safety Rating, Initial Cost, Resale Value, Emission Rating] and the population mean [metric].

In order to run this statistical design, I would need a dataset containing the averages of the metrics I want to test on for both the MechaCar model(s) along with the same information for all cars that're in the same class as those.  All of the metrics I wish to run are numeric and readily available, so that shouldn't be much of an issue to acquire. 
