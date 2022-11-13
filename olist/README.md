![mer](https://raw.githubusercontent.com/pauloreis-ds/olist/main/business_questions_insights/images/mer.png)

## Metadata

**Attention**

- An order might have multiple items.
- Each item might be fulfilled by a distinct seller.
- All text identifying stores and partners where replaced by the names of Game of Thrones great houses.


### olist_customers_dataset.csv

This dataset has information about the customer and its location.<br>
Use it to identify unique customers in the orders dataset and to find the orders delivery location.

At our system each order is assigned to a unique customerid.<br>
This means that the same customer will get different ids for different orders.<br>
The purpose of having a customerunique_id on the dataset is to allow you to identify<br>
customers that made repurchases at the store. Otherwise you would find that each<br>
order had a different customer associated with.

**customer_id**: key to the orders dataset. Each order has a unique customer_id.

**customer_unique_id**: unique identifier of a customer.

**customer_zip_code_prefix**: first five digits of customer zip code

**customer_city**: customer city name

**customer_state**: customer state


### olist_geolocation_dataset.csv

This dataset has information Brazilian zip codes and its lat/lng coordinates.<br>
Use it to plot maps and find distances between sellers and customers.


**geolocation_zip_code_prefix**: first 5 digits of zip code

**geolocation_lat**: latitude

**geolocation_lng**: longitude

**geolocation_city**: city name

**geolocation_state**: state


### olist_order_items_dataset.csv

This dataset includes data about the items purchased within each order.

**order_id**: order unique identifier

**order_item_id**: sequential number identifying number of items included in the same order.

**product_id**: product unique identifier

**seller_id**: seller unique identifier

**shipping_limit_date**: Shows the seller shipping limit date for handling the order over to the logistic partner.

**price**: item price

**freight_value**: item freight value item (if an order has more than one item the freight value is splitted between items)

### olist_order_payments_dataset.csv

This dataset includes data about the orders payment options.

**order_id**: unique identifier of an order.

**payment_sequential**: a customer may pay an order with more than one payment method. If he does so, a sequence will be created to accommodate all payments.

**payment_type**: method of payment chosen by the customer.

**payment_installments**: number of installments chosen by the customer.

**payment_value**: transaction value.

### olist_order_reviews_dataset.csv

This dataset includes data about the reviews made by the customers.<br>
After a customer purchases the product from Olist Store a seller gets notified<br>
to fulfill that order. Once the customer receives the product, or the estimated<br>
delivery date is due, the customer gets a satisfaction survey by email where he can<br>
give a note for the purchase experience and write down some comments.


**review_id**: unique review identifier

**order_id**: unique order identifier

**review_score**: Note ranging from 1 to 5 given by the customer on a satisfaction survey.

**review_comment_title**: Comment title from the review left by the customer, in Portuguese.

**review_comment_message**: Comment message from the review left by the customer, in Portuguese.

**review_creation_date**: Shows the date in which the satisfaction survey was sent to the customer.

**review_answer_timestamp**: Shows satisfaction survey answer timestamp.

### olist_orders_dataset.csv

This is the core dataset. From each order you might find all other information.

**order_id**: unique identifier of the order.

**customer_id**: key to the customer dataset. Each order has a unique customer_id.

**order_status**: Reference to the order status (delivered, shipped, etc).

**order_purchase_timestamp**: Shows the purchase timestamp.

**order_approved_at**: Shows the payment approval timestamp.

**order_delivered_carrier_date**: Shows the order posting timestamp. When it was handled to the logistic partner.

**order_delivered_customer_date**: Shows the actual order delivery date to the customer.

**order_estimated_delivery_date**: Shows the estimated delivery date that was informed to customer at the purchase moment.

### olist_products_dataset.csv

This dataset includes data about the products sold by Olist.

**product_id**: unique product identifier

**product_category_name**: root category of product, in Portuguese.

**product_name_lenght**: number of characters extracted from the product name.

**product_description_lenght**: number of characters extracted from the product description.

**product_photos_qty**: number of product published photos

**product_weight_g**: product weight measured in grams.

**product_length_cm**: product length measured in centimeters.

**product_height_cm**: product height measured in centimeters.

**product_width_cm**: product width measured in centimeters.

### olist_sellers_dataset.csv

This dataset includes data about the sellers that fulfilled orders made at Olist.<br>
Use it to find the seller location and to identify which seller fulfilled each product.

**seller_id**: seller unique identifier

**seller_zip_code_prefix**: first 5 digits of seller zip code

**seller_city**: seller city name

**seller_state**: seller state

### product_category_name_translation.csv

Translates the productcategoryname to english.

**product_category_name**: category name in Portuguese

**product_category_name_english**: category name in English


[Original Source](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce?select=olist_order_items_dataset.csv)
