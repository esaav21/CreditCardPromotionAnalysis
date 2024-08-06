# Credit Card Promotion Test Analysis

## Project Overview

This project involves analyzing a credit card promotion experiment conducted by a bank with 1,000 of its Small Business owner customers. The bank aimed to determine whether a special Low Fee promotion would entice customers to apply for their credit card. The dataset contains information on customer credit scores, whether they received the promotional offer, and whether they applied for the credit card.

## Dataset

The dataset "CreditCardPromotionData.csv" includes the following columns:

- **Customer ID:** Unique identifier for each customer.
- **Credit Score Tier:** Credit quality of the customer (High = 1, Mid = 2, Low = 3).
- **Potential Outcomes 0:** Imaginary outcomes assuming no promotion (Didn't Apply = 0, Applied = 1).
- **Potential Outcomes 1:** Imaginary outcomes assuming promotion (Didn't Apply = 0, Applied = 1).
- **Actual Outcomes:** Actual observed outcomes (Didn't Apply = 0, Applied = 1).
- **Offer Letter Sent:** Whether the customer received the offer letter (Didn't Receive Offer Letter = 0, Received Offer Letter = 1).

## Analysis Objectives

The main objectives of this analysis are to estimate the Average Treatment Effects (ATE), their Standard Errors, and 95% Confidence Intervals for actual outcomes. The analysis is conducted on the total sample and by credit score tier. Additionally, the blocking technique using credit scores is applied to understand its impact on the results.

### Key Findings

1. **Overall Sample:**
   - The ATE for the total sample was found to be 0.283 with a standard error of 0.035. The 95% confidence interval is [0.216, 0.351].

2. **By Credit Score Tier:**
   - **Tier 1 (High):** ATE = -0.052, SE = 0.016, 95% CI = [-0.084, -0.021]
   - **Tier 2 (Mid):** ATE = -0.034, SE = 0.017, 95% CI = [-0.068, -0.001]
   - **Tier 3 (Low):** ATE = 0.087, SE = 0.021, 95% CI = [0.046, 0.127]

3. **Blocking Technique:**
   - The combined ATE using the blocking technique was found to be 0.300 with a standard error of 0.025. The 95% confidence interval is [0.250, 0.350].

### Additional Insights

1. **Differences between Credit Score Tiers:**
   - Customers with low credit scores (Tier 3) showed the highest positive response to the promotion, while those with high credit scores (Tier 1) had a negative response.
   - This suggests that the promotion was more effective among customers with lower credit quality.

2. **Blocking Technique:**
   - Using the blocking technique provided a more refined estimate of the treatment effect, indicating the importance of considering customer segments when analyzing promotional impacts.

## Recommendations

- **Targeted Promotions:** Consider targeting future promotions more towards customers with lower credit scores (Tier 3), as they showed the highest positive response.
- **Segmented Analysis:** Use blocking or segmentation techniques in future analyses to gain a deeper understanding of how different customer segments respond to promotions.
