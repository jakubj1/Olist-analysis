This is a Brazilian ecommerce public dataset of orders made at Olist Store. The dataset has information of 100k orders from 2016 to 2018 made at multiple marketplaces in Brazil. Its features allows viewing an order from multiple dimensions: from order status, price, payment and freight performance to customer location, product attributes and finally reviews written by customers. We also released a geolocation dataset that relates Brazilian zip codes to lat/lng coordinates.

This is real commercial data, it has been anonymised, and references to the companies and partners in the review text have been replaced with the names of Game of Thrones great houses.

Given the vast scope of the data, it is needed to narrow the focus specifically
to the shoes category for a targeted analysis. This process involved the use of SQL and
Excel for data manipulation and Tableau for visualization purposes.
The primary datasets utilized in this analysis were “orders”, “order_items”, and “products”.
These datasets were merged into a single table using a left join operation in SQL. The
product categories, initially in Portuguese, were translated into English using the
“product_translation” dataset, making it more accessible. Upon checking the amount of
orders by each product category, shoes category is chosen, by using count function for the
order_id columns from the “orders” dataset. For the joined table that was created, additional
filter is added using where function for product category “fashion_shoes”, to receive only data
for the shoes category.
Additionally, the month names were extracted from the 'order_purchase_timestamp' using
the monthname function, and a new column 'price_total' was created. This new column
represents the total cost incurred by the customer, calculated by summing the product price
and delivery fee (freight value), and rounding the result to two decimal places.

The newly created table was joined by additional datasets—“order_payments”,
“customers”, and “order_reviews” using the left join operation. The final, filtered dataset was
exported to Excel and then to Tableau for visualization.
