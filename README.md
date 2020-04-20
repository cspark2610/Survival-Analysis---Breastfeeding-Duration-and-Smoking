## Methods

## Data Source 
Data were used from a study conducted to examine factors related to breast feeding. The data consisted of 927 mother-infant pairs for which the mothers chose to breastfeed their children, the children were born after 1978, at gestational ages between 20-45 weeks.  

## Overview of Measures
Density plots and histograms were produced for continuous and factor variables, respectively. The density plot for minimum duration of breastfeeding and time on study (length) indicated that there was evidence of normal distribution. There were far higher subjects who completed the study than those who did not (complete). It was shown that there were more Whites than Others and Blacks, with Blacks having the lowest number of participants (race). A greater number of mothers were not in poverty (poverty), had not smoked (smoke), or consumed alcohol while pregnant (alcohol), and had not sought out prenatal care within the first 3 months of pregnancy (prenatal3), compared to their counterparts. Mother’s age at child birth were normally distributed (age) and babies were found to be born mostly between 1980-1985 (birthyr). Years of mothers’ education were also found to be normally distributed (educ). 

For this analysis, length and complete are the outcome measures and smoke will be used as the primary predictor to assess the factors related to duration of breastfeeding. Smoke will be treat as a factor variable (0=Did not smoke during pregnancy; 1=Smoked during pregnancy).

## Descriptive Analysis
Kaplan-Meier estimator was used to estimate survival function for each predictor over time. Kaplan-Meier plots were constructed for every Kaplan-Meier estimate for visualization. Log-log 95% confidence intervals were used to provide the most precise measurements.

## Two-Group Comparison
From the survival plots, it was apparent that a large number of events or failures occurred earlier in the study than later. Therefore, Gehan-Wilcoxon tests were performed to test whether there were any differences in survival between groups for each predictor; Gehan-Wilcoxon are more sensitive to earlier differences between survival curves than the more commonly used Log-rank test.

## Model Selection
Stepwise regression was performed to determine predictors for the adjusted Cox Proportional-Hazards model (Cox PH). The stepwise regression model was calibrated to select initial covariates at an alpha of 0.2, then at a final alpha of 0.1 for multivariate analysis. Due to having large number of tied events, all Cox Proportional-Hazards models used Efron approximations, which yield closer estimates than the Breslow method. Age was the only predictor forced into the stepwise model. Loglikelihood and AIC values were calculated for non-adjusted and adjusted models to assess model fit.
## Evaluating linearity of age effects
To evaluate linearity of age effects, Cox PH models were performed for each transformation of the, age, predictor. Age was transformed as continuous, square root, categorical, ordinal, linear and quadratic, and linear and quadratic and cubic. Age categories were defined as three groups based on quantiles; less than or equal to 20 years old, greater than 20 and less than 23 years old, and greater than or equal to 23 years old. Age was square rooted for square root transformation. Age was squared for quadratic term and cubed for cubic term. Loglikelihood and AIC values were used to assess model fit.

Final Cox Proportional-Hazards included all significant predictors from the stepwise regression model and cubic transformed age. 

## Proportional Hazards Assumption
Scaled Schoenfeld’s residuals against time were plotted for each predictor. However, to confirm if whether the assumption holds or not Martingale’s Residuals for the fitted final adjusted Cox PH model was also plotted to examine whether residuals were spread evenly over time. Lastly, a log-log Kaplan-Meier against log time was plotted to show whether any crossovers or non-parallel lines were evident. 

## Sample Size Calculation for 80% Power 
To obtain the sample size calculation to have 80% power to detect the observed hazard ratio for mothers who smoke and who do not, with a two-significance level of 0.05, the following equation can be used.
 
d = required # of events
z_1-α\/2 = Z values for confidence of intervals
z_(1-β) = Power (%)
θ = HR

 
## Results

## Overview of Measures
Density plots and histograms were produced for continuous and factor variables, respectively. The density plot for minimum duration of breastfeeding and time on study (length) indicated that it was normally distributed. There were much larger number of those who completed the study than those who did not (complete). There were more Whites than Others and Blacks, with Blacks having the lowest number of participants (race). A greater number of mothers were not in poverty (poverty), had not smoked (smoke), or consumed alcohol while pregnant (alcohol), and had not sought out prenatal care within the first 3 months of pregnancy (prenatal3), compared to their counterparts. Mother’s age at child birth were normally distributed (age) and babies were found to be born mostly between 1980-1985 (birthyr). Years of mothers’ education were also found to be normally distributed. 

## Descriptive Survival Analyses
Survival function estimates were conducted using Kaplan-Meier, which were plotted. The plots indicate that number of events or failures occur early into the study, as shown in Figure 1. In addition, it is apparent from the plot that, on average, mothers’ who had smoked during pregnancy had a lower survival probability compared to mothers’ who had not. Moreover, early into the study there is evidence of several crossovers between the two groups survival probability, but begins to increase the gap between 20 and 50 weeks, roughly. 

### Figure 1. Kaplan-Meier Survival Plot of Mothers who did or did not engage in smoking during pregnancy. 
![alt text](https://github.com/cspark2610/Survival-Analysis---Breastfeeding-Duration-and-Smoking/blob/master/images/figure_1.png)

## Two-Group Comparison – Gehan’s Wilcoxon Test
Due to having earlier differences for survival, two-group comparisons were conducted using Gehan-Wilcoxon’s test as opposed to the Log-rank test. At an alpha of 0.05, the survival estimates between smoke and non-smoke group was found to be statistically significant (p-value <0.004). Moreover, race (p-value =0.008) and educ (p-value =0.04) were also found to be statistically significant in having group differences in survivability. 	

## Model Selection
Stepwise regression was conducted to select predictors of interest for the adjusted Cox PH model. As shown in Table 1, the predictors that were selected for the adjusted model were birthyr, smoke, race, educ, and poverty, while age was forced into the model which was not statistically significant. Forward selection was used to keep statistically significant predictors. Efron’s approximation was used due to overcome the large number of ties and tends to yield better estimates than the Breslow method. 

![alt text](https://github.com/cspark2610/Survival-Analysis---Breastfeeding-Duration-and-Smoking/blob/master/images/table_1.JPG)
![alt text](https://github.com/cspark2610/Survival-Analysis---Breastfeeding-Duration-and-Smoking/blob/master/images/table_1_2.JPG)

Loglikelihood ratio and AIC tests were used to assess model fit. The unadjusted model presented an AIC of 10375.05 while the adjusted model presented an AIC of 10349.98. Additionally, the loglikelihood ratios differed by 35.2. The adjusted model produced lower AIC values, therefore, it is indicated that the adjusted model is a better model for prediction than the unadjusted model for smoking.

## Evaluating Linearity of Age Effects
Adjusted Cox-PH models were conducted for each transformed age predictor. Likelihood ratio and AIC values were calculated to evaluate the best parameterization of age for prediction. The values were very similar across both likelihood ratios and AIC, as shown in Table 2. However, the cubic transformation of age presented the lowest AIC and lower loglikelihood ratio values than linear and quadratic transformations of age. 

![alt text](https://github.com/cspark2610/Survival-Analysis---Breastfeeding-Duration-and-Smoking/blob/master/images/table_2.JPG)
![alt text](https://github.com/cspark2610/Survival-Analysis---Breastfeeding-Duration-and-Smoking/blob/master/images/table_2_2.JPG)


## Final Cox PH Adjusted Model
The final adjusted Cox PH model included smoke, age_cubic, age_quad, age, birthyr, race, educ, and poverty. The final output is displayed in Table 3. 

![alt text](https://github.com/cspark2610/Survival-Analysis---Breastfeeding-Duration-and-Smoking/blob/master/images/table_3.JPG)


As shown in Table 3, all predictors were statistically significant (alpha <0.05), with the exception of being black (race2). The overall Cox PH model was statistically significant at p-value < 0.001. Smoking while pregnant increased the hazard of whether breastfeeding was completed by 29.9%. A year increase in infant’s birthyear increased hazard by 8.3%. Compared to Whites, mothers from an “Other” race were subject to a 36% increase in hazard. A year increase of mothers’ education was associated with a 5% decrease in hazard. Mothers who gave birth while in poverty was associated with a 19% decrease in hazard.
Figure 2. Final Adjusted Survival Curve for Cox PH Model to estimate Breastfeeding for Mothers who Had or Had Not Smoked During Pregnancy  
After visualizing the adjusted survival curves for the final Cox PH Model, as shown in Figure 2, it is apparent that there are less crossovers between the two groups than the unadjusted Kaplan-Meier Plot (Figure 1). The factors that were used to adjust smoking in the final Cox PH Model increased the separation between the two groups. Since, the survival curves do not have a larger number of crossovers we can proceed with testing for proportional hazards assumption.

## Testing Proportional Hazards Assumption
All Schoenfeld residual plots against time were not statistically significant with exception of educ (p =0.0363).  Therefore, the proportional hazards assumption does not mildly hold. However, from visualizing the residual plot for educ against time, the residuals are evenly spaced along the X-axis and the fitted line is horizontal throughout. Subsequently, Martingale residuals against time for the final adjusted Cox PH model was produced to investigate whether the assumption holds.

### Figure 3. Plots of Schoenfeld Residuals of Predictors Against Time
![alt text](https://github.com/cspark2610/Survival-Analysis---Breastfeeding-Duration-and-Smoking/blob/master/images/figure_3.png)


### Figure 4. Martingale Residuals of All Predictors Against Time 	
![alt text](https://github.com/cspark2610/Survival-Analysis---Breastfeeding-Duration-and-Smoking/blob/master/images/figure_4.png)





### Figure 5. Survival Plot and Log-Log Survival Plot Against Time for Breastfeeding and Smoke Status
![alt text](https://github.com/cspark2610/Survival-Analysis---Breastfeeding-Duration-and-Smoking/blob/master/images/figure_5.png)

 
Figure 4, depicts a horizontal fitted line within Martingale Residuals against time. Several outliers are salient, however, majority of the residuals are spread evenly across the X-axis,  akin to the Scaled Individual Schoenfeld residuals plot. Finally, a log-log survival curve against log of time was plotted and shown in Figure 5. The survival curves have a few crossovers in the beginning and end of the duration, however, with the exception of two crossovers in the middle time period, the hazards remained fairly proportional. 

## Sample Size Calculation for 80% Power 
To obtain the sample size calculation for 80% statistical power, the following equation was used. 

![alt text](https://github.com/cspark2610/Survival-Analysis---Breastfeeding-Duration-and-Smoking/blob/master/images/cohens_d.JPG)

d = required number of events
z_1-α\/2 = 1.96
z_(1-β) = 0.84 (for 80%)
ln(θ) = 1.254846

d=(4(1.96+0.84)^2 )\/([ln(1.25486)]^2 )
d = 608.5 = 609 events

The sample size needed to have 80% power to detect observed hazard ratios for mothers who smoked or did not during pregnancy with a two-sided alpha of 0.05, requires 609 events. However, this come with a caveat, this only holds true if no censoring occurred throughout the study. Therefore, censoring needs to be accounted for survival analysis. 

## Conclusion
Analyses were conducted, analyzed, and interpreted to help examine the factors that come into play with duration of breastfeeding. Kaplan-Meier estimator was performed and plotted for duration of breastfeeding and time by whether mothers’ did or did not smoke while pregnant. Confidence intervals were outlined through “log-log” method, since it delivered the most precise 95% confidence interval bands. It was apparent from the KM plot that majority of the events or failures occurred earlier on during the study; therefore, to test whether survival differences between groups were significant or not, Gehan’s-Wilcoxon test was used to predict statistical significance. Race, education, and smoking were predictors that were statistically significant from Wilcoxon test.

Stepwise Regression was performed to select covariates for the final adjusted model. Age was forced into the stepwise regression, and at an alpha of 0.2 initial covariates were selected, then lastly, at an alpha of 0.1 covariates were selected to be included in final multivariate model. These covariates were birthyear, smoke, race, educ, poverty and age, which were all statistically significant, except for age, and improved model fit. Model fit were assessed using -2LogL and AIC values. The adjusted model showed improvement with having lower AIC and -2LogL values than the unadjusted model.

To evaluate linearity of age effects, age was transformed into continuous, square root, categorical, ordinal, linear and quad, linear and quad and cubic. After, reviewing AIC and -2LogL values, it was concluded that age as linear, quad, and cubic form presented best model fit; therefore, the final adjusted Cox PH model included age as linear quad, and cubic. 

The final adjusted Cox PH model found all predictors to be statistically significant, except for being Black. Education, poverty, and age in cubic and linear form decreased hazards of completing breastfeeding, while the other measures were associated with an increase in hazards. The final model was statistically significant at p-value <0.001. Mothers’ smoking status while pregnant or not, mothers’ race, mothers’ education, and mothers’ poverty status were found to be factors that are related to duration of breastfeeding. Age was only statistical significant when transformed to quad and cubic forms. So, age has a very low relationship with breastfeeding.

To test whether the assumption of Proportional Hazards was met, scaled Schoenfeld’s Residuals over time were plotted for each predictor. Only education was found to be statistically significant, which would indicate that the assumption is not met, however, the visual plot of education residuals over time did not strongly highlight the significance. Therefore, Martingale’s Residuals for the fitted final Cox PH model was plotted against time, which supported the findings of the Schoenfeld’s Residuals plot. The fitted line was almost fully horizontal and residuals were evenly distributed across the horizontal Axis. Lastly, a log-log of the survival function over log time by smoking status was plotted to assess whether the lines were parallel or not. The lines were not parallel in the beginning and at the end of the study period, however, the middle portion was close to indicating proportional hazards. However, there is not enough of evidence to show that the assumption for proportional hazards was met.

Sample size calculations were performed to have a power of 80% to detect hazard ratios for mothers who smoke or do not at a two-sided significance of 0.05. The final calculations led to the conclusion that, if no censoring occurs during the study, 609 events must occur to have 80% power.
