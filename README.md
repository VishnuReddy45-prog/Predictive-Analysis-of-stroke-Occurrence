# Predictive-Analysis-of-stroke-Occurrence using SAS

This project utilizes SAS to predict stroke risk based on key demographic and health variables like age, hypertension, heart disease, BMI, and smoking status. Using Chi-square tests and binary logistic regression, it identifies significant predictors and moderation effects. Findings help improve healthcare interventions and insurance risk assessments. The study highlights the role of predictive modeling in stroke prevention and policymaking.

The Dataset consists of 10 metrics for a list of Patients. These metrics included Patients health records (hypertension, heart disease, average glucose level, body mass index (BMI), smoking status and history of stroke) as well as their demographic information (gender, age, marital status, kind of employment and residence type).

This dataset’s Primary goal is to predict stroke for individual patients who are at higher risk based on various variables. It can be accomplished by:

Identifying Risk Factors: By analyzing the relationships between variables like age, hypertension, heart disease, and stroke occurrence. Researchers can identify the key factors that increase stroke risk.

Purpose

Developing Predictive Models: Using their demographic and health information, we can fit models to this data to estimate a person’s risk of stroke.
Developing Predictive Models: Using their demographic and health information, we can fit models on this data to estimate a person’s risk of stroke.
Monitoring Stroke Risk: Monitoring an individual’s stroke risk can be improved by tracking changes in these variables over time.

The Dataset includes the following variables:
![image](https://github.com/user-attachments/assets/613fe371-223f-461a-b80b-0f86cf03c1a1)  
![image](https://github.com/user-attachments/assets/b0aad80c-2673-4024-896d-c01860196a5b)

Problem Statement-1

We checked if there is a moderation effect between age and metabolic health indicators (such as heart_disease, BMI, and average glucose level) that influence stroke risk across the different populations ? 
Method Used: Binary logistic Regression with moderation effect
Predictor Variables: heart_disease, age
Outcome Variable: Stroke

Conceptual Diagram of the moderation effect:

Moderation Effect: A moderation effect, also known as an interaction effect, occurs when the relationship between two variables changes depending on the level or presence of a third variable. The effect of one variable on an outcome is influenced by the presence or level of another variable.

![image](https://github.com/user-attachments/assets/44159028-bbaf-47e0-a637-5a2f35099d2d)

Initial Assumptions:

    Null Hypothesis(H0): No moderation effect?   
    Alternate Hypothesis(H1): There is a moderation effect?
    
![image](https://github.com/user-attachments/assets/9fba4027-6e83-4c9f-8078-ca8dd0edc34c)

Conclusion on the moderation effect:

As we can see, the p-value for heart_disease is less than 0.005, so we can reject the null hypothesis. Indicating they are significant predictors of brain stroke, and that there is a moderation effect of heart disease on the relationship between age and brain stroke risk. 

We checked if there is a moderation effect between age and metabolic health indicators (such as heart_disease, BMI, and average glucose level) that influence stroke risk across the different populations? 

Method Used: Binary logistic Regression with moderation effect
Predictor Variables: BMI, age
Outcome Variable: Stroke

![image](https://github.com/user-attachments/assets/693d89c5-e5dc-4ea6-971d-a5a9b5c5dfc7)

Initial Assumptions:
 Null Hypothesis(H0): No moderation effect?
 Alternate Hypothesis(H1): There is a moderation effect?

![image](https://github.com/user-attachments/assets/bb58f099-f07f-4f75-babe-e7bb5a2fe1b4)

Conclusion on the moderation effect: 

As we can see, the p-value for BMI is less than 0.005, so we can reject the null hypothesis. Indicating they are significant predictors of brain stroke, and that there is a moderation effect of BMI on the relationship between age and brain stroke risk. 

Summary of Interpretation:

In summary, the logistic regression model with the interaction term provides insights into how age, BMI, and their interaction influence the likelihood of the event occurring. It highlights the importance of considering the interaction effect when examining the relationship between predictor variables and the outcome variable, leading to a better understanding of the factors contributing to the event of interest.

We checked if there is a moderation effect between age and metabolic health indicators (such as heart_disease, BMI, and average glucose level) that influence stroke risk across the different populations?

Method Used: Binary logistic Regression with moderation effect
Predictor Variables: avg_glucose_level, age
Outcome Variable: Stroke

![image](https://github.com/user-attachments/assets/83407219-ae30-4960-8e26-20f26ef85926)

Initial Assumptions:
 Null Hypothesis(H0): No moderation effect?
 Alternate Hypothesis(H1): There is a moderation effect?
 
![image](https://github.com/user-attachments/assets/0ae9e8a1-f524-4839-b73c-1c2b6eee1cd6)

 Conclusion on the moderation effect: 

As we can see, the p-value for avg_glucose_level is less than 0.005, so we can reject the null hypothesis. Indicating they are significant predictors of brain stroke, and that there is a moderation effect of  avg_glucose_level on the relationship between age and brain stroke risk. 

Summary of Interpretation:

In summary, the logistic regression model with the interaction term provides insights into how age, avg_glucose_level, and their interaction influence the likelihood of the event occurring. It highlights the importance of considering the interaction effect when examining the relationship between predictor variables and the outcome variable, leading to a better understanding of the factors contributing to the event of interest.

Problem statement-2

Does smoking affect the likelihood of having a stroke among individuals within a given population?
Model used - chi-square: The chi-square test is commonly used to evaluate the association between categorical variables. In this case, we want to determine whether there is a significant relationship between smoking status and stroke occurrence

Hypothesis: 
Null Hypothesis (H0): Smoking status and stroke occurrence are independent (i.e., no association). 
Alternative Hypothesis (H1): Smoking status and stroke occurrence are dependent (i.e., there is an association).

![image](https://github.com/user-attachments/assets/ab9f80b0-5c01-4f24-949f-65f3a24adc9e)

χ² = Formula: χ² = Σ ((O - E)² / E) 
Where: χ² is the chi-square statistic, 
O is the observed frequency, 
E is the expected frequency (To calculate the expected frequency value: E = Row Total * Column Total / Total number of observations
DF = (number of smoking status categories - 1) *(number of stroke occurrence categories - 1)
Chi-square calculated value = 34.65. 
Critical value = CHISQ.INV.RT(0.05,2) = 5.99 
Since Chi-square calculated value = 34.65 > Critical value = 5.99. It will be in the rejection region; hence, we will reject the null hypothesis. 

![image](https://github.com/user-attachments/assets/ad73116c-f6d1-49d3-805a-46ca81c651c1)

Alternatively, the p-value is less than 0.0001 (indicated as “<0.0001” in the table), so we reject the null hypothesis.

Conclusion

This means that there is a significant association between smoking status and stroke occurrence in the given population.
In practical terms, this suggests that smoking status may indeed affect the likelihood of having a stroke. Individuals who smoke (either currently or formerly) may be at a different risk level compared to those who have never smoked.

Problem Statement-3

How can health insurance providers optimize premium calculation and personalized healthcare interventions based on predictive models, considering various health indicators and demographic variables, to effectively predict the likelihood of stroke risk among insured individuals while ensuring cost-effectiveness and improved health outcomes?

Model Used: Binary logistic regression with Backward elimination of predictor variables.
Variables: hypertension, heart_disease, avg_glucose_level, bmi, age, gender, ever_married, work_type, Residence_type, smoking_status
![image](https://github.com/user-attachments/assets/1cddf05e-f300-4685-b050-964e47c02c0d)

Low p-value, therefore, reject the null hypothesis on the model level 

![image](https://github.com/user-attachments/assets/af120d14-0f81-4566-ac33-e94345af9bec)

For the R-squared value of 0.1723, it signifies that about 17.23% of the variance in stroke occurrence can be elucidated by the predictor variables included in the model, such as age, hypertension, heart disease, average glucose level, and smoking status. However, a substantial portion of the variability remains unaccounted for, implying the potential presence of additional factors beyond those considered in this analysis that contribute to the likelihood of experiencing a stroke.

![image](https://github.com/user-attachments/assets/d721cad8-6146-47a2-9ddf-019c692c32a1)

The fitted model is:

![image](https://github.com/user-attachments/assets/9c3987ab-ad5e-4e98-8cca-3e91a66fecd5)

Estimated probability of experiencing a stroke 

Odds Ratios:
Hypertension:
Odds Ratio: 2.030
Interpretation: Individuals with hypertension have approximately 2.030 times higher odds of experiencing a stroke compared to those without hypertension, holding other variables constant.
Heart Disease:
Odds Ratio: 2.143
Interpretation: Individuals with heart disease have approximately 2.143 times higher odds of experiencing a stroke compared to those without heart disease, holding other variables constant.
Average Glucose Level:
Odds Ratio: 1.003
Interpretation: For each one-unit increase in average glucose level, the odds of experiencing a stroke increase by approximately 1.003 times, holding other variables constant.
Age:
Odds Ratio: 1.073
Interpretation: For each one-year increase in age, the odds of experiencing a stroke increase by approximately 1.073 times, holding other variables constant.
Smoking Status (Formerly Smoked vs. Smokes):
Odds Ratio: 0.747
Interpretation: Individuals who formerly smoked have approximately 0.747 times the odds of experiencing a stroke compared to those who currently smoke, holding other variables constant.
Smoking Status (Never Smoked vs. Smokes):
Odds Ratio: 0.774
Interpretation: Individuals who never smoked have approximately 0.774 times the odds of experiencing a stroke compared to those who currently smoke, holding other variables constant.
These interpretations provide insights into how each predictor variable affects the odds of experiencing a stroke, holding other variables constant.

Summary of Interpretation:

The logistic regression model estimates the log odds of experiencing a stroke based on various predictor variables such as age, hypertension, heart disease, average glucose level, and smoking status.
Age, hypertension, heart disease, and average glucose level are positively associated with increased odds of experiencing a stroke, meaning individuals with higher values for these variables are at higher risk.
Formerly smoked and never-smoked categories of smoking status are negatively associated with the odds of experiencing a stroke, indicating that individuals who formerly smoked or never smoked have lower odds compared to current smokers.

Insights and Recommendations for Health Insurance Providers:

1. Risk Assessment: Age, hypertension, heart disease, and average glucose level are significant predictors of stroke risk. Health insurance providers can use this information to assess the risk profile of individuals applying for health plans. Those with higher risk factors may require more comprehensive coverage or additional health management programs.
2. Premium Calculation: Individuals with higher risk factors, such as older age, hypertension, heart disease, and elevated glucose levels, may be charged higher premiums to reflect their increased likelihood of experiencing a stroke. Conversely, individuals who formerly smoked or never smoked may be eligible for lower premiums due to their lower risk profile.
3. Personalized Healthcare Interventions: Health insurance providers can use this model to identify high-risk individuals and offer personalized healthcare interventions aimed at stroke prevention. This may include targeted wellness programs, lifestyle modifications, and regular health screenings to mitigate stroke risk factors.
4. Data Integration: Continuously updating the model with additional data sources, such as electronic health records and lifestyle data, can improve its predictive accuracy. Health insurance providers can collaborate with healthcare providers to integrate these data sources and enhance risk assessment capabilities.
5. Promoting Healthy Behaviours: By highlighting the impact of lifestyle factors such as smoking status on stroke risk, health insurance providers can incentivize healthy behaviours through wellness initiatives and rewards programs. Encouraging smoking cessation and promoting healthy lifestyle choices can contribute to overall risk reduction and improved health outcomes.
Incorporating these insights into risk assessment, premium calculation, and personalized healthcare interventions can help health insurance providers better manage stroke risk among insured individuals and ultimately improve health outcomes while optimizing cost-effectiveness.


































 



























