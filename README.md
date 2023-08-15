# *Customer Churn Rate*
---
The following codes below answers the questions asked in the project statement slide

/* Count of customers that have done two or more product */
SELECT COUNT(customer_id)
FROM (SELECT customer_id, COUNT(Id) AS number_of_transaction
FROM `inter-387014.NETIN.Payment Table Final`
GROUP BY customer_id
HAVING COUNT(Id) >= 2)


