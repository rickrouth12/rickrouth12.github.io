---
layout: post
title:      "Optimizing Food Distribution Through Data Analytics"
date:       2019-05-20 23:21:29 -0400
permalink:  optimizing_food_distribution_through_data_analytics
---


Businesses can be well-oiled machines operating at full capacity and yet still have room to grow. Other companies harbor sharp inefficiencies that detract from an organization’s ability to survive. It takes determined leaders to pave the clear path to success and longevity, but behind every leader is a team of analysts that leverages data to steer a company’s leadership toward making more informed decisions. It starts with a series of questions and access to raw data and it ends with insights, innovation, and progress.
 
**Data Set:** Northwinds Database – Food Distribution Product Orders
* Categories
* Customers
* Employees
* Employee Territories
* Order Details
* Orders
* Products
* Region
* Shippers
* Suppliers
* Territories
 
**Product Pricing Strategies**
So, as a member of this analytics team, I will start with a question:
Do discounts have a statistically significant effect on the number of food products our customers order? If so, what level(s) of discount are most impactful?
 
**Part 1:**
We can attack this question by first formulating a null and alternative hypothesis as part of Statistical Hypothesis Testing. Statistical Hypothesis Testing, is a statistical inference technique used to compare two datasets, or a sample from a dataset, to then draw a conclusion. That conclusion can be used to make more informed decisions to improve a business.

**Null Hypothesis:** The average quantity of products ordered is the same for fully priced items and those with discounts applied.
<br>
**Alternative Hypothesis:** The average quantity of products ordered differs between orders with full price items and those with discounts applied.

We will move forward and plan to conduct a two-sample, two-tailed set of statistical tests between the control group (fully priced orders) and experimental group (discounted orders) to validate our drawn conclusion or answer to the above question.
![(https://imgur.com/REVFctY)]

Key Assumptions to Check to Validate Our Conclusions:
Normality, Equal Sample Size, Equal Variance

**Normality**
![(https://imgur.com/lu2ld7o)]
![(https://imgur.com/WWJXNEc)]
 
By confirming the similar variance and sample sizes we can then leverage a Student’s T-Test in order to effectively compare these two data sets. Here we find a p-value within the alpha threshold of 0.05. 
 
**Conclusion:**
Now we can reject the null hypothesis and accept the alternative hypothesis with evidence to support our assertion that discount levels do have a significant effect on the average quantity per order.

**Part 2:**
We can take our first question a step further by asking: Are some discount levels more effective at increasing the total gross sales for our sales team?
 
**Null Hypothesis:** The average quantity of products ordered is the same for all discount levels.
<br>
**Alternative Hypothesis**: The average quantity of products ordered differs between orders with varying discount levels.
 ![(https://imgur.com/yezGZN5)]
 
To test our normality assumption, we will need to run normal tests for each of these discount levels. 
![(https://imgur.com/vuQQ7fZ)]
 
After running these tests, I have found that none of the data sets represent normal distributions. 
![(https://imgur.com/z7rGANW)]
 
But, they do have similar measures of variance.
 
In order to test the statistical significance, I will use Welch’s T-Test which provides a more forgiving comparison by increasing the degrees of freedom which are incorporated. 
![(https://imgur.com/UTUGjjn)]
 
The Welch’s T test results produce p-values all within the alpha threshold of 0.05. 

**Conclusion:**
We can now accept our alternative hypothesis that each discount level individually impacts the quantity of products per order sold.
 
We can follow the same framework to ask and answer more questions about our food distribution business leveraging statistical testing to substantiate our findings.
 
**Sales Performance** - Do the members of our sales team perform equally in terms of the quantity of products sold? How about total sales?
 
**Customer Buying Trends** - Are reorder levels effective indicators of popular products?
 
**Shipping and Distribution** - Does the region of the customer versus the region of the supplier impact the shipping prices associated with the freight for these orders?

**Summary**

Statistical significance and hypothesis testing tools enable analysts to validate assertions, provide evidence, and present a more compelling case to executive leadership to then make smarter decisions every day. I asked a number of questions and walked through in detail how to data about how my company’s sales team prices our food products involving discount levels to incentivize customers to purchase high-quality food. I have concluded that discount levels do affect the quantity of products sold per order and each individual discount level is significant in that relationship. We can now use this information to focus more on the individual deltas we are seeing in order to maximize profits by reducing our need to discount items in order to complete a successful customer order. 

