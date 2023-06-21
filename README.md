# Clients-Credit-Card

# Analysis of Customer Segmentation in a Bank

**Abstract:**
This study focuses on analyzing customer behavior and segmenting customers based on their banking and credit card usage data. The goal is to utilize machine learning algorithms, such as the K-means algorithm, to identify distinct customer groups. The results of the segmentation analysis reveal variations in balance and credit usage, purchase behavior, cash advances, and credit limit and payments among different customer groups.

**Introduction:**
Understanding customer behavior is crucial for banks to develop effective marketing strategies, personalized services, and risk management approaches. This study aims to explore customer segmentation based on their financial activities, allowing the bank to tailor its offerings to different customer groups. By utilizing machine learning algorithms, we can identify meaningful patterns and insights from the available data.

**Methodology:**
This case requires to develop a customer segmentation to define marketing strategy. The sample Dataset summarizes the usage behavior of about 9000 active credit card holders during the last 6 months. The file is at a customer level with 18 behavioral variables.

Following is the Data Dictionary for Credit Card dataset :

- `CUST_ID` : Identification of Credit Card holder (Categorical)
- `BALANCE` : Balance amount left in their account to make purchases
- `BALANCE_FREQUENCY` : How frequently the Balance is updated, score between 0 and 1 (1 = frequently updated, 0 = not frequently updated)
- `PURCHASES` : Amount of purchases made from account
- `ONEOFF_PURCHASES` : Maximum purchase amount done in one-go
- `INSTALLMENTS_PURCHASES` : Amount of purchase done in installment
- `CASH_ADVANCE` : Cash in advance given by the user
- `PURCHASES_FREQUENCY` : How frequently the Purchases are being made, score between 0 and 1 (1 = frequently purchased, 0 = not frequently purchased)
- `ONEOFFPURCHASESFREQUENCY` : How frequently Purchases are happening in one-go (1 = frequently purchased, 0 = not frequently purchased)
- `PURCHASESINSTALLMENTSFREQUENCY` : How frequently purchases in installments are being done (1 = frequently done, 0 = not frequently done)
- `CASHADVANCEFREQUENCY` : How frequently the cash in advance being paid
- `CASHADVANCETRX` : Number of Transactions made with "Cash in Advanced"
- `PURCHASES_TRX` : Numbe of purchase transactions made
- `CREDIT_LIMIT` : Limit of Credit Card for user
- `PAYMENTS` : Amount of Payment done by user
- `MINIMUM_PAYMENTS` : Minimum amount of payments made by user
- `PRCFULLPAYMENT` : Percent of full payment paid by user
- `TENURE` : Tenure of credit card service for use

The analysis involved applying the K-means algorithm to segment customers based on their banking and credit card data. This algorithm clusters customers into groups based on similarities in their financial behavior. The results provide valuable insights into the distinct characteristics of each customer segment.

For the determination of the number of clusters in the K-means algorithm, the elbow method has been employed. This technique involves plotting the variance explained by the algorithm against the number of clusters, forming an elbow-like curve. The number of clusters is determined by identifying the point on the curve where the incremental gain in variance explained begins to level off significantly, resembling the bend of an elbow. In this case, the elbow method analysis suggests that the optimal number of clusters is 4.

In addition, the silhouette coefficient has been utilized to support this decision. The silhouette coefficient measures how well each data point fits within its assigned cluster, taking into account both the cohesion and separation of the clusters. By calculating the average silhouette coefficient for different numbers of clusters, we can determine the number that maximizes the overall quality of clustering. In this analysis, the silhouette coefficient suggests that 2 clusters are a viable option, followed closely by 4 clusters. However, considering the small difference between them and our interest in having more than 2 distinct groups, 4 clusters have been chosen as the final partitioning.

Therefore, based on both the elbow method and the silhouette coefficient, the consensus is that the optimal number of clusters for this K-means algorithm is 4, as it aligns with the preference for having more than 2 distinct groups while taking into account the suggestions provided by the silhouette coefficient.

![image](https://github.com/JorgeMiGo/Clients-Credit-Card/assets/127945994/738c5236-805d-439f-8428-ff72a537a5ad)

![image](https://github.com/JorgeMiGo/Clients-Credit-Card/assets/127945994/511e6d85-83fd-458e-8d1b-30dab54c362f)


**Segmentation Results:**

**1. Balance and Credit Usage:**
- Group 2 exhibits the highest average balance (3,589.19$), followed by Group 0 (4,652.62$). This indicates that these groups have more funds available in their accounts for making purchases.
- Group 3 has the lowest average balance (915.83$), suggesting that these customers may have lower purchasing power.

**2. Purchase Behavior:**
- Group 2 shows the highest average purchase amount (7,843.31$) and also has the highest average number of purchase transactions (90.84). This indicates that this group makes larger and more frequent purchases.
- Group 1 demonstrates the lowest values in terms of average purchase amount (275.04$) and average number of purchase transactions (3.03). These customers engage in less frequent and lower-value purchases.

**3. Cash Advances:**
- Group 0 exhibits the highest average cash advance amount (4,582.46$) and also the highest frequency of cash advances. This could indicate a higher reliance on cash advances for financial needs within this group.
- Group 1 has the lowest average cash advance amount (603.97$) and frequency. This suggests that these customers have less need for cash advances.

**4. Credit Limit and Payments:**
- Group 2 has the highest average credit limit (9,758.31$), indicating a greater credit capacity for these customers.
- Group 3 has the lowest average credit limit (4,266.37$), suggesting relatively limited credit capacity.
- In terms of payments, Group 2 demonstrates the highest average payment amount (7,464.10$), while Group 1 shows the lowest average payment (1,013.02$). This could indicate a difference in payment capacity and financial discipline among the groups.

In summary, different customer groups exhibit distinctive financial behavior characteristics. While Group 2 stands out with high balance, purchase amounts, and credit limit, Group 1 has lower balances and purchase activity. Group 0 shows a more frequent use of cash advances, while Group 3 has lower credit limits and payment amounts. These differences suggest varying credit risk profiles and financial behavior among the customer groups.

By understanding the financial behavior of different customer segments, the bank can develop targeted strategies to meet the specific needs and preferences of each group. This segmentation analysis provides valuable insights for marketing campaigns, product development, and risk management strategies within the bank.
