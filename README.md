# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG

Questions to answer

Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

- MPG (which of course, is the intercept), vehicle length, along wtih ground clearance are the variables that provided a non-random amount of variance to predicting the MPG values. 

Is the slope of the linear model considered to be zero? Why or why not?

- No, the slope of the linear model is not zero.  This is because our p-value is  < alpha level of 0.05 meaning that we reject the null hypothesis that the slope of the linear model is zero.

Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

- No, afraid not.  While the multiple R-squared value is .7149, which means that the linear model is able to correctly predict the MPG value of a car in *this* dataset 71% of the time, the intercept is statistically significant, which means that there are outstanding variables that are contributing to the variation in our model.  This is an issue because we ran all of our available variables in our multiple linear model, so we cannot begin to explain what hidden variable(s) are influencing MPG values.  Without that information, I would not be comfortable saying that the model we created can predict MPG values for cars in this dataset, and it definitely doesn't seem to have a solid level of external validity.

## Deliverable 2

## Summary Statistics on suspension coils

question: The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

- The current manufacturing data shows that unfortunately, the requirement that the variance of the suspension not exceed 100 pounds per square inch (PSI) is not being observed by the brain genuises in Lot 3.  As the summary shows, they currently have a variance of 170.28, which not only exceeds the perscribed maximum by more than 70 PSI, but it's also way out of line with the variance that we're observing in Lot 1 and 2.  Those two lots' variance levels for suspension PSI is but a fraction of Lot 3's levels.  Whatever they're doing in Lot 3 to have such unacceptable PSI variance, is an isolated issue to that specific Lot.
