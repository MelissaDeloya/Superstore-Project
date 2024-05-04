
## Write a SQL query that orders the items by price.

SELECT the columns item and price
FROM the table superstore
ORDER the data BY the column price



## Price for items in the category of "Kitchen Supplies"

 

SELECT avg(price)

FROM superstore

WHERE category="Kitchen Supplies";

 

## Sum of Air Purifiers 

SELECT sum(stock_quantity)

FROM superstore

WHERE item_name = "Air Purifier";
 

 
