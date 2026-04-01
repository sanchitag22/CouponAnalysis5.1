# CouponAnalysis5.1
Coupon Analysis

# 1. Problem Statement

Objective:
The goal of this analysis is to analyze customer behavior to understand which factors influence coupon acceptance. Using exploratory data analysis (EDA), we identify patterns across demographics, behavior, and context to determine which customers are most likely to accept coupons.

We aim to:

Understand patterns in customer behavior
Analyze how contextual, demographic, and behavioral variables impact acceptance
Generate actionable insights for targeted marketing strategies

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
**6.1. Data Subset**
Filter dataset for Bar coupons

**Purpose:**
Focus analysis on a single coupon type for deeper insights

**6.2. Acceptance Rate**
Calculate acceptance rate for bar coupons

**Goal:**
Compare with overall acceptance

**6.3. Behavioral Analysis**
**Bar Visit Frequency**
Compare acceptance: 
 ≤3 visits/month
 3 visits/month

**Age-Based Analysis**
Compare: Age >25 vs others

**Passenger Type**
Compare: With kids vs without kids 

**Occupation**
Compare: Farming vs non-farming

**Key Insight Theme:**
Behavior + lifestyle influence acceptance

**6.4. Advanced Segmentation**
Combine multiple conditions: Frequent visitors, Age, Passenger type, Income

Goal:
Identify high-converting customer segments

**6.5. Key Insights (Bar Coupons)**

Frequent bar-goers → higher acceptance

Social/flexible lifestyle → higher engagement

Demographics enhance targeting

# 7. Independent Investigation: Coffee Coupons

**7.1. Data Subset:** Filter dataset for Coffee House coupons

**7.2. Acceptance Rate:** Calculate overall coffee coupon acceptance

**7.3. Time-Based Analysis:** 

Acceptance by time of day
  Insight Focus: Morning vs evening behavior

**7.4. Passenger Analysis:**

Acceptance by passenger type
  Insight Focus: Social vs family context

**7.5. Behavioral Analysis:**

Acceptance by coffee visit frequency
  Insight Focus: Habit-driven behavior

**7.6. Key Insights (Coffee Coupons):**

Frequent coffee drinkers → highest acceptance
Time of day matters (morning stronger)
Social context influences decisions

# 8. Key Findings:

Overall coupon acceptance rate: 56.84%

**Bar Coupons**
Overall acceptance: 41%
Frequent bar visitors (>3 times/month): 76.88%
Infrequent visitors (≤3 times/month): 37.06%
Impact: +39% higher acceptance for frequent visitors

**Age + Behavior Impact**
Frequent bar-goers (age >25): 69.52%
Others: 33.50%
Impact: +36% higher acceptance

**Lifestyle Impact**
Frequent bar-goers without kids: 71.32%
Others: 29.60%
Impact: +41% higher acceptance

**Coffee Coupons**
Overall acceptance: 49.92%
Frequent coffee visitors (4–8 times): 68.6%
Rare visitors: 48.2%
Never visit: 18.9%
Impact: Regular users are ~3.5× more likely to accept

**Time of Day**
Highest acceptance: 10 AM (~64%)
Lowest acceptance: 10 PM (~42%)
Impact: Timing drives ~20% variation


# Key Findings
Overall coupon acceptance rate is ~57%, indicating moderate engagement.

Behavioral patterns are the strongest predictor. Frequent coffee/bar visitors show significantly higher acceptance rates.

Time of day and passenger type influence decisions. Younger users, non-family travelers, and lower/mid-income groups show higher engagement.

# Conclusion
Customers who already engage in activities like visiting bars or coffee shops are significantly more likely to accept related coupons. For example, frequent bar visitors had nearly double the acceptance rate compared to infrequent visitors. Similarly, regular coffee drinkers were far more responsive than those who never visit coffee shops.

Demographics and context also play an important role. Customers over 25, those without kids, and those in more flexible social settings showed higher acceptance rates. Additionally, timing matters, with coupons performing best when they align with natural habits (e.g., coffee in the morning).

On the other hand, customers who do not typically engage in the activity or whose lifestyle does not align with the coupon (e.g., traveling with kids or rarely visiting bars/coffee shops) are much less likely to accept offers.

Overall, the key takeaway is that targeted and behavior-driven marketing is far more effective than generic promotions. By focusing on the right customer segments at the right time, businesses can significantly improve coupon acceptance and engagement.
