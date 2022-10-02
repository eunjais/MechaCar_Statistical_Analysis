# MechaCar_Statistical_Analysis

## Overview

Utilizing R, the datasets for MechaCar are visualized in basic plots and statistical tests (T-Test, linear regression) for an in-depth analysis of the given dataset.

- dplyr library
- R studio
- tidyverse

## Linear Regression to Predict MPG

![lin_reg](https://user-images.githubusercontent.com/107447038/193476562-6db829dd-5afc-4f3b-aae7-87ea9e9d3c1e.png)

![sum_lin_reg](https://user-images.githubusercontent.com/107447038/193476578-f6dd38e9-386e-4205-ad23-a3328075842e.png)

Given the 95% level of confidence, p-value compared to alpha = 0.05 level of significance allows for us to determine whether the given variance is statistically significant. 

Coefficients are as follows:
- mpg: 0 < 0.05 statistically significant, non-random amount of variance
- vehicle length: 0 < 0.05 statistically significant, non-random amount of variance
- vehicle weight: 0.08 > 0.05 not statistically significant, random amount of variance
- spoiler angle: 0.31 > 0.05 not statistically significant, random amount of variance
- ground clearance: 0 > 0.05 statistically significant, non-random amount of variance
- AWD: 0.19 >= 0.05 not statistically significant, random amount of variance


mpg = -.01 + 6.267(vehicle length)+.001(vehicle weight)+.069(spoiler angle)+3.546(ground clearance)-3.411(AWD) is the multiple linear regression formula which has a non-zero slope. 

R(2) is equal to 0.72 which shows a strong correlation between the dataset and allows us to conclude that it is effective. Further statistical analysis is required, however, of the various other variables to ensure that the MechaCar prototype mpg model prediction is as accurate as possible.

## Summary Statistics on Suspension Coils

![all_lots_2_1](https://user-images.githubusercontent.com/107447038/193476759-0ac8f332-b03b-49a1-9242-ead117ddbefb.png)

Above shows the statistical summary of all manufacturing lots. The population mean = 1500

![manufactoring_lot_summary_2](https://user-images.githubusercontent.com/107447038/193476794-6d698a78-05d7-46c0-a024-fc5738656741.png)

Above shows the summary by manufacturing lot numbers, 1-3. 

Overall, the collective of manufacturing lots show that variance is 62 < 100, which is acceptable and stays under the specification of the suspension coil variance not exceeding 100 lbs per square inch. However, in-depth analysis of individual lots show that while Lot 1 and Lot 2 have acceptable values of 0.98 and 7.47 respectively, Lot 3's variance exceeds the limit with a staggering 170.29. 


## T-Tests on Suspension Coils
![t_test_all_lots_3_1](https://user-images.githubusercontent.com/107447038/193476896-d432f1bf-d2fb-4783-bfcd-3b0755c20f71.png)

The parameters:
- p-value: 0.0628
- alpha: 0.05

The t-test results of all manufacturing lots show that the mean is within the 95% confidence level. However, 0.60 > 0.05; This implies that the total manufacturing lot is not statistically significant from the normal distribution.

![t_test_lot_1](https://user-images.githubusercontent.com/107447038/193476902-4aafcce7-f7c9-45a1-a8c0-987b5b839f6e.png)

Lot 1 parameters:
- p-value = 1
- alpha: 0.05

1 > 0.05; this lot is also not statistically significant but the mean still falls within the 95% confidence interval.

![t_test_lot_2](https://user-images.githubusercontent.com/107447038/193476908-c5efbe94-3bc3-432f-97fc-7e343cc71c8f.png)

Lot 2 parameters:
- p-value = 0.6072
- alpha: 0.05

0.61 > 0.05; this lot is also not statistically significant but the mean still falls within the 95% confidence interval.

![t_test_lot_3](https://user-images.githubusercontent.com/107447038/193476912-0c9a73f6-3b93-4f6e-b2bc-8c9b24de3d11.png)

Lot 3 parameters:
- p-value = 0.04168
- alpha: 0.05

0.042 < 0.05; this lot is statistically significant from the normal distribution. The mean falls within the 95% interval.

Lot 1 and Lot 2, in conclusion, show a normal distribution and statistic similarity. We cannot rerject the null hypothesis.


## Study Design: MechaCar vs Competition

Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.

In your description, address the following questions:

What metric or metrics are you going to test?
What is the null hypothesis or alternative hypothesis?
What statistical test would you use to test the hypothesis? And why?
What data is needed to run the statistical test?
