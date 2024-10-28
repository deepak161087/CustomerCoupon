# Customer Coupons: Will the Customer accept the coupon?

**Context**

Imagine driving through town and a coupon is delivered to your cell phone for a restaurant near where you are driving. Would you accept that coupon and take a short detour to the restaurant? Would you accept the coupon but use it on a subsequent trip? Would you ignore the coupon entirely? What if the coupon was for a bar instead of a restaurant? What about a coffee house? Would you accept a bar coupon with a minor passenger in the car? What about if it was just you and your partner in the car? Would weather impact the rate of acceptance? What about the time of day?

Obviously, proximity to the business is a factor on whether the coupon is delivered to the driver or not, but what are the factors that determine whether a driver accepts the coupon once it is delivered to them? How would you determine whether a driver is likely to accept a coupon?

**Overview**

The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not.

**Data**

This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’.  There are five different types of coupons -- less expensive restaurants (under \$20), coffee houses, carry out & take away, bar, and more expensive restaurants (\$20 - $50).


### Observations Summary for Bar Coupons

1. **Acceptance Rates by Visit Frequency:**
   - Drivers who visit bars **3 or fewer times** a month have an acceptance rate of **36.93%**.
   - Drivers who visit bars **more than 3 times** a month have a significantly higher acceptance rate of **76.53%**.

2. **Age and Acceptance Rates:**
   - Acceptance rate for drivers **over 25 years old** who go to bars more than once a month is **69.00%**.
   - Acceptance rate for **all other drivers** is much lower at **33.00%**.

3. **Additional Conditions:**
   - Acceptance rate for drivers who visit bars **more than once a month**, **not traveling with kids**, and **not in farming occupations** is **71.00%**.
   - Acceptance rate for **all other drivers** is only **29.00%**.

4. **Condition-Based Acceptance Rates:**
   - Condition 1 (Bars > 1 month, Not a kid, Not widowed): **69.00%** acceptance rate.
   - Condition 2 (Bars > 1 month and Age < 30): **72.00%** acceptance rate.
   - Condition 3 (Restaurants > 4 times a month and Income < 50K): **45.00%** acceptance rate.
   - **Combined Acceptance Rate** for all conditions is **57.00%**.

**Hypothesis on driver who accept Bar coupons:**

1. Drivers who visit bars more frequently have a significantly higher acceptance rate for bar coupons compared to those who visit less often.
2. Older drivers (over 25) are more likely to accept bar coupons than younger drivers.
3. The presence of children and occupation may negatively impact the acceptance rate of bar coupons.
4. Various conditions, such as age and restaurant visit frequency, also play a role in determining coupon acceptance, indicating that lifestyle factors influence the likelihood of coupon acceptance.


### Observations Summary for Coffee House Coupons
1. Acceptance rates for drivers who go to coffee houses more than once a month vary by temperature:
   - At 30°F, the acceptance rate is **54.55%**.
   - At 55°F, the acceptance rate increases to **58.50%**.
   - At 80°F, the acceptance rate further increases to **71.51%**.

2. Acceptance rates for drivers who go to coffee houses more than once a month vary by marital status:
   - Divorced individuals have an acceptance rate of **60.00%**.
   - Married partners have a rate of **66.18%**.
   - Singles have a higher acceptance rate of **67.70%**.
   - Unmarried partners have an acceptance rate of **62.31%**.

3. Drivers under 21 who go to coffee houses more than once a month have an acceptance rate of **75.00%**, which is significantly higher than the acceptance rate of **49.00%** for all other drivers.

4. Acceptance rates based on coffee house visits:
   - 1-3 times: **64.72%**
   - 4-8 times: **68.24%**
   - Greater than 8 times: **65.79%**
   - Less than once: **48.26%**
   - Never: **17.52%**

**Hypothesis on driver who accept Coffee House coupons:**
1. There is a positive correlation between temperature and coupon acceptance rates among drivers who frequently visit coffee houses.
2. Marital status influences acceptance rates, with single individuals showing the highest acceptance rates.
3. Younger drivers (under 21) have a higher tendency to accept coupons compared to older drivers.
4. Increased frequency of coffee house visits is associated with higher acceptance rates for coupons.

### Recommendations and Next Steps
***Targeted Marketing Strategies:***
Create targeted campaigns aimed at demographics with higher acceptance rates (e.g., young adults under 21, frequent bar visitors) to maximize coupon usage.

***Enhanced Promotions:***
Consider bundling coffee house coupons with bar visits for customers who frequent both venues to encourage increased engagement.

***Real-Time Monitoring:***
Establish a dashboard to monitor coupon acceptance rates over time, allowing for timely adjustments to marketing strategies based on observed trends.

***User Experience Improvements:***
Gather feedback from customers on their experiences with coupon redemption and identify areas for improvement, such as simplifying the process or increasing incentives.

***Collaborate with Marketing Teams:***
Work closely with marketing and sales teams to align insights from the analysis with promotional strategies, ensuring that campaigns are data-driven and targeted effectively.