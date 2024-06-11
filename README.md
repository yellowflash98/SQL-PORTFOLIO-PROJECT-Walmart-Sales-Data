Added Queries and Analyses:
Customer Type VAT Contribution:

Added a query to identify which customer type pays the most in VAT.
sql
Copy code
SELECT customer_type, AVG(VAT) AS VAT
FROM sales
GROUP BY customer_type
ORDER BY VAT DESC;
Unique Customer Types:

Added a query to count how many unique customer types exist in the data.
sql
Copy code
SELECT DISTINCT customer_type FROM sales;
Unique Payment Methods:

Added a query to count how many unique payment methods exist in the data.
sql
Copy code
SELECT DISTINCT payment_method FROM sales;
Customer Type Purchase Volume:

Added a query to determine which customer type buys the most.
sql
Copy code
SELECT customer_type, COUNT(*) AS cstm_cnt FROM sales
GROUP BY customer_type;
Customer Gender Distribution:

Added a query to identify the gender distribution of customers.
sql
Copy code
SELECT gender, COUNT(*) AS gender_cnt FROM sales
GROUP BY gender
ORDER BY gender DESC;
Gender Distribution by Branch:

Added a query to determine gender distribution per branch.
sql
Copy code
SELECT gender, COUNT(*) AS gender_cnt FROM sales
WHERE branch = "c"
GROUP BY gender
ORDER BY gender DESC;
Customer Ratings by Time of Day:

Added a query to identify what time of day customers give the most ratings.
sql
Copy code
SELECT time_of_day, COUNT(rating) AS cnt_rating FROM sales
GROUP BY time_of_day
ORDER BY cnt_rating DESC;
Ratings by Time of Day per Branch:

Added a query to determine which time of the day customers give the most ratings per branch.
sql
Copy code
SELECT time_of_day, AVG(rating) AS avg_rating FROM sales
WHERE branch = "c"
GROUP BY time_of_day
ORDER BY avg_rating DESC;
Best Average Ratings by Day of the Week:

Added a query to find out which day of the week has the best average ratings.
sql
Copy code
SELECT day_name, AVG(rating) AS avg_rating
FROM sales
GROUP BY day_name
ORDER BY avg_rating DESC;
Structure and Cleanup:
The existing queries and analyses from walmartsalesSQL.txt were retained, and new queries were integrated seamlessly.
Enhanced the breadth of data analysis by adding new dimensions related to customer behavior, gender distribution, and rating patterns.
By incorporating these additional queries, the walmartsalesSQL.final.txt file now offers a more comprehensive analysis of sales data, focusing on customer behavior, payment methods, and ratings, which provides deeper insights for business decisions.
