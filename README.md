# CouponAnalysis5.1

# 1. Problem Statement

Objective:
Analyze customer behavior to understand which factors influence coupon acceptance. Using exploratory data analysis (EDA), we identify patterns across demographics, behavior, and context to determine which customers are most likely to accept coupons.

Goal:
  1. Understand patterns in customer behavior
  2. Analyze how contextual, demographic, and behavioral variables impact acceptance
  3. Generate actionable insights for targeted marketing strategies

# 2.Source: 
UCI Machine Learning Repository
Collected via Amazon Mechanical Turk survey
Contains driving scenarios + coupon decisions

# 3. Data Loading and Overview
**Tasks:**
  1. Import required libraries:pandas, matplotlib, seaborn
  2. Load dataset (coupons.csv)
  3. Inspect structure of data
     
**Key Checks:**
  1. First few rows → head()
     
  2. Data types and nulls → info()
    
  3. Summary statistics → describe()

**Purpose:**

To understand the dataset before performing cleaning and analysis.

# 4. Data Cleaning
The dataset was inspected for missing and problematic values before analysis. The car column contained mostly missing values and was removed. Several behavioral frequency columns (such as visits to bars, coffee houses, and restaurants) had missing values, which were handled by imputing them as “never,” since missing values likely indicate no visits. Overall, the dataset required minimal cleaning and was suitable for exploratory analysis after these adjustments.

**Steps:**

**4.1. Handle Missing Values**

  Identify columns with missing values,
  Replace missing values in behavioral columns with "never"
  
**4.2. Dropped car column**

**4.3. Validate Data**
Check remaining missing values,
Confirm no unintended data loss

**Purpose:**

Ensure data quality and consistency before proceeding to analysis.

# 5. Exploratory Data Analysis (EDA)
**5.1. Overall Coupon Acceptance**

  Compute overall acceptance rate and Understand baseline performance
  
**Insight Focus:**
 What proportion of users accept coupons?

**5.2. Coupon Distribution**
  Bar plot of coupon column

**What to analyze:**
  Which coupon types are most frequent and any imbalance in dataset

**Expected Insight:**

  Dataset is skewed toward certain coupon types (e.g., Coffee House)

# 6. Bar Coupon Analysis

Frequent bar visitors are significantly more likely to accept coupons, indicating strong behavioral alignment.
Drivers over 25 with regular bar visits show higher acceptance rates, suggesting age and lifestyle influence decisions.
Customers without kids (more flexible/social context) are more responsive to bar coupons.
Combining behavior + demographics (age, passenger, occupation) further improves targeting effectiveness.

**Key Takeaway**

Bar coupon acceptance is highest among socially active, frequent bar-goers, making behavioral targeting the most effective strategy.

# 7. Independent Investigation: Coffee Coupons

Frequent coffee house visitors have the highest acceptance rates, showing strong habit-driven behavior.
Acceptance varies by time of day, with higher engagement during typical coffee consumption hours (e.g., morning).
Drivers traveling alone or with friends are more likely to accept coupons, indicating social context matters.
Customers who rarely visit coffee houses show low engagement, suggesting weaker relevance of the offer.

**Key Takeaway**

Coffee coupon acceptance is driven by routine behavior and timing, with frequent users in flexible or social settings showing the highest engagement.

# 8. Key Findings:

**_Overall coupon acceptance rate: 56.84% indicating moderate engagement._**

**Bar Coupons**
  1. Overall acceptance: 41%
  2. Frequent bar visitors (>3 times/month): 76.88%
  3. Infrequent visitors (≤3 times/month): 37.06%
     
Impact: +39% higher acceptance for frequent visitors

**_Behavioral patterns are the strongest predictor. Frequent coffee/bar visitors show significantly higher acceptance rates._**

**Age + Behavior Impact**
  1. Frequent bar goers (age >25): 69.52%
  2. Others: 33.50%
     
Impact: +36% higher acceptance

**Lifestyle Impact**
  1. Frequent bar goers without kids: 71.32%
  2. Others: 29.60%
     
Impact: +41% higher acceptance

**Coffee Coupons**
  1. Overall acceptance: 49.92%
  2. Frequent coffee visitors (4–8 times): 68.6%
  3. Rare visitors: 48.2%
  4. Never visit: 18.9%
     
Impact: Regular users are ~3.5× more likely to accept

**_Time of day and passenger type influence decisions. Younger users, non family travelers, and lower/mid income groups show higher engagement._**

**Time of Day**
  1. Highest acceptance: 10 AM (~64%)
  2. Lowest acceptance: 10 PM (~42%)
     
Impact: Timing drives ~20% variation

# Statistical Interpretation
  1. Behavioral variables (CoffeeHouse frequency) show the strongest correlation with acceptance.
  2. Contextual factors (time, passenger type) further influence customer decisions.
  3. The relationship between frequency and acceptance suggests a positive trend (monotonic increase),  higher usage leads to higher acceptance.

# Conclusion
Customers who already engage in activities like visiting bars or coffee shops are significantly more likely to accept related coupons. For example, frequent bar visitors had nearly double the acceptance rate compared to infrequent visitors. Similarly, regular coffee drinkers were far more responsive than those who never visit coffee shops.

Demographics and context also play an important role. Customers over 25, those without kids, and those in more flexible social settings showed higher acceptance rates. Additionally, timing matters, with coupons performing best when they align with natural habits (e.g., coffee in the morning).

On the other hand, customers who do not typically engage in the activity or whose lifestyle does not align with the coupon (e.g., traveling with kids or rarely visiting bars/coffee shops) are much less likely to accept offers.

Overall, the key takeaway is that targeted and behavior driven marketing is far more effective than generic promotions. By focusing on the right customer segments at the right time, businesses can significantly improve coupon acceptance and engagement.

# Actionable Recommendations
  1. Target frequent coffee consumers for higher ROI
  2. Optimize coupon timing (e.g., morning hours)
  3. Personalize offers based on passenger context
  4. Use behavioral segmentation instead of broad campaigns

# Next Steps
  1. Build a predictive model to identify high probability customers
  2. Run A/B tests on targeted vs general campaigns
  3. Incorporate real time signals (location, time, past behavior)
  4. Expand analysis to other coupon types for broader strategy

