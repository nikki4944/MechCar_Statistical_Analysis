# MechCar_Statistical_Analysis
Statistics and R

## Project Overview
The client, AutosRUs, has asked for a statistical analysis of the production data of their prototype, MechaCar, to assist their manufacturing team in producing completed prototypes. Using R script, I performed statistical analysis on two csv files provided by the client, a suspension coil data set and a MechaCar data set.  

## Linear Regression to Predict MPG

Using the MechaCar data set provided by the client, I performed a linear regression analysis. The csv file included data on six different vehicle features: vehicle length, vehicle weight, spoiler angle, ground clearance, all wheel drive, and miles per gallon (MPG). 

The following imnage shows the results of the statistical analysis performed using MPG as the dependent variable and the remaining features as the independent variable:

<img width="526" alt="MPG Linear Regression" src="https://user-images.githubusercontent.com/82982901/129459832-8009e4ff-77a8-4ccb-b7c5-73a778491200.png">

#### Summary of Linear Regression Model

The individual p-values  of less than 0.05% indicate variables with a non-random amount of variance. In this case, the independent variables of vehicle weight and ground clearance meet this requirement. The variables with random amount of variance are vehicle weight, spoiler angle, and all wheel drive. This indicates that vehicle weight and ground clearance have a significant impact on miles per gallon for the MechaCar prototypes.

The p-value for the overall model is 5.35e-11 which is smaller than the assumed significance value of 0.05% indicating the slope of the linear model is not zero.

The linear model is moderately successful at predicting mpg of MechaCar prototypes as the r value is .715. Models with an r value greater than .5 are considered to be effective for predicting.

## Summary Statistics on Suspension Coils

The design specifications for MechaCar suspension coils dictate the variance cannot exceed 100 pounds per square inch. Using the summarize() function in R on the provided suspension coil data set, I created two summary tables to determine the variance for total PSI and then further broke down the data to determine variance PSI for each of the three manufacturing lots.

As illustrated in the below image, the variance PSI for the total manufacturing lots is 62.29 which is within the limits for compliance.
<img width="279" alt="Screen Shot 2021-08-14 at 6 49 00 PM" src="https://user-images.githubusercontent.com/82982901/129462076-3693d2fc-3e71-4233-b76c-8d0f1ca04fd5.png">

As illustrated in the below image, the variance PSI for Lot 3 is 170.286 which is above the limits for compliance. Lots 1 and 2 are .979 and 7.469 respectively, well below the compliance requirements.
<img width="435" alt="Screen Shot 2021-08-14 at 6 49 28 PM" src="https://user-images.githubusercontent.com/82982901/129462080-d1b248c3-3931-4b1e-82c1-2ab56064f18f.png">

## T-Tests on Suspension Coils


## Study Design: MechaCar vs Competition
