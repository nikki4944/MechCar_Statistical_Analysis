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

In order to determine if the manufacturing lots are statistically different from the population mean of 1,500 pounds per square inch as determined in the prior summary, I ran t.tests on the suspension coil data set provided by the client.

First, I ran a t.test compairing all the manufacturing lots with the population mean of 1,500 and received a p-value of 0.06 as shown below. Given this result, it is possible to determine that the means are statistically similar, assuming a standard significance level of 0.05.

<img width="414" alt="Screen Shot 2021-08-14 at 8 31 19 PM" src="https://user-images.githubusercontent.com/82982901/129463569-bfabeddd-2e9f-4638-9d6f-714e46203052.png">

In order to run a t.test comparing each individual lot, a small tweak was made to the code used previously. The code in the above image was a paired t.test; however, a t.test which subsets the data for each individual lot is an unpaired t.test and requires the use of the subset argument. As shown below, after running the adjusted t.test code for each lot, it is possible to determine that the means are statistically similar for lots 1 and 2 which have p-values greater than 0.05 but lot 3 has a mean that is not statistically similar with a calculated p-value of .04. 

<img width="512" alt="Screen Shot 2021-08-14 at 8 51 01 PM" src="https://user-images.githubusercontent.com/82982901/129463638-5179ac6d-6645-4074-9615-deea0753e2f7.png">


## Study Design: MechaCar vs Competition

The above statistical analysis is most useful for internal applications, especially in assisting the manufacturing team meet their production deadlines. However, the average consumer will not be interested in a statistical analysis based on PSI data. In order to expand the application of R and statistical analysis to assist AutosRUs in applealing to consumers, a further report is recommended which compares MechaCar data with its competitors for highway fuel efficiency. 

For this proposed study design, the null hypothesis assumes the MechaCar has a mean of 40 miles per gallon highway. To test this, we would calculate the mean miles per gallon highway reported for all of the MechaCar prototypes. We would then compare the result of this calculation to 40, the assumed, or claimed, mean using the resulting p-values of one-sample t.test to accept or reject the null hypothesis.

Similarly, using a one-sample t.test, it would be possible to determine how the MechaCar's highway fuel efficiency differs statistically from its competition. The data for this test would be a data set consistenting of reported highway miles per gallon, or highway fuel efficiency, for the MechaCar and its competitors.
