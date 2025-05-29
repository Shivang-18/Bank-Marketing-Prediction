# Bank-Marketing-Prediction

The primary challenge addressed in this study revolves around the direct marketing campaigns conducted by a Portuguese bank. These campaigns predominantly utilize phone calls as a medium to promote term deposits among clients. The core objective is to develop a predictive model that reliably forecasts whether a client will subscribe to a term deposit, constituting a binary classification problem.
The dataset crucial to this study encapsulates data from these marketing campaigns, including comprehensive records of 45,211 instances, each detailed across 16 attributes. These attributes provide a multi-faceted view of each client’s demographic and financial status, as well as their interaction history with the bank’s marketing efforts. The outcome of the predictive model is expected to enhance the efficiency and effectiveness of future marketing campaigns by allowing for more targeted and personalized client approaches.

## Exploratory Data Analysis

### 1. Correlation Heatmap for Continuous Variables
   
- Objective:
  The correlation heatmap was generated to identify relationships among continuous features such as age, balance, duration, campaign, day, pdays, and previous. This step       helps in assessing potential multicollinearity, ensuring that redundant variables do not negatively impact the predictive model.

![corr plot](https://github.com/user-attachments/assets/8d61e82e-d499-41be-848a-72aeb47347ca)

- Insight:
  The heatmap reveals that the correlations between most of the continuous variables are quite low, with values ranging from -0.11 to 0.14. This indicates that the features 
  exhibit weak linear relationships with one another. The absence of strong correlations among the majority of variables implies that each feature captures distinct 
  information and can independently contribute to the predictive model.


### 2. Age Distribution by Subscription Status (Histogram)
   
- Objective:
  The age distribution histogram was plotted to analyse how the age of customers relates to their likelihood of subscribing to the product (represented by the binary target    variable y). This visualization helps determine whether certain age groups are more inclined to subscribe.

  ![image](https://github.com/user-attachments/assets/0b5fc253-5719-4ea0-bbdb-78b1a7da2d86)

- Insight:
  The histogram shows that most customers fall within the 25-40 age group, with a gradual decline in the number of customers as age increases beyond 50 years. However, the 
  distribution of subscription responses is heavily skewed toward "no" responses (non-subscribers) across all age groups. This imbalance suggests that a large proportion of 
  customers contacted during the campaign were not interested in subscribing.

- Impact on Modelling:
  The observed imbalance between "yes" and "no" responses will influence the model development process. Specifically, oversampling techniques like SMOTE (Synthetic Minority 
  Oversampling Technique) may be applied to address the class imbalance and ensure that the model does not become biased toward predicting non-subscription.


### 3. Contact Duration by Job Type

The boxplot illustrates the distribution of call duration (in seconds) segmented by different job types, providing insight into the relationship between the client’s profession and subscription status. Several key observations emerge from this plot:

   ![image](https://github.com/user-attachments/assets/64cc7232-66ab-42a1-b2a5-c3f50ce327e3)

- Impact of Call Duration: Across all job categories, individuals who subscribed (represented by the orange box) tend to have a higher median call duration compared to those 
  who did not subscribe (green box). This trend reinforces the idea that longer interactions with clients are correlated with a higher probability of subscription.

- Variation Across Job Types:
  
  - Management and entrepreneur roles display significantly higher durations among subscribers, suggesting these professions might require extended communication to achieve      subscription success.
    
  - Students and unemployed clients exhibit shorter durations for both categories (subscription and non-subscription), potentially indicating that these groups may be less       responsive to long sales calls.
    
  - Blue-collar clients exhibit wide variability in call duration, which could reflect a more heterogeneous response pattern.

## Conclusion

Profession is a significant factor influencing call duration and, consequently, subscription rates. Campaign strategies should consider tailoring the length of interactions based on the client’s job type, ensuring efficiency without compromising conversion opportunities.


