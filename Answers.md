# DB-Assignment


1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram

Answer: After looking at the diagram. It seems or depicts that the link between "Product" and "Product_Category" is like this: one product can be in one category, but one category can have lots of products.
Let's consider a simple example for this:
Imagine we have a picture that shows different things we can buy, like a bunch of products. Each of these products is put into a category, like "Electronics" or "Clothes." Now, the connection between a specific product (let's say a phone) and its category (like "Electronics") is like a rule. The rule says that one phone belongs to one category, but that category can have many different phones in it.

So, it's a bit like sorting your toys into boxes. Each toy goes into one box, but each box can hold many toys. That's how the "Product" and "Product_Category" are related in the picture. One thing fits into one group, but that group can have lots of things in it. Thats all.







2. How could you ensure that each product in the "Product" table has a valid category assigned to it?

Answer: To ensure that each product in the "Product" table has a valid category assigned to it, we would typically use a foreign key constraint. 
By doing with an example, we can create a foreign key constraint in SQL which will look something like this


ALTER TABLE Product
ADD CONSTRAINT fk_product_category
FOREIGN KEY (category_id)
REFERENCES Product_Category(id);


This will add a foreign key constraint named "fk_product_category" to the "Product" table, specifying that the "category_id" column must reference the "id" column in the "Product_Category" table.
By doing this, the database will ensure that any value in the "category_id" column of the "Product" table must exist in the "id" column of the "Product_Category" table, thus enforcing the relationship between products and their categories. If an attempt is made to insert a product with a non-existent category ID, or if a category referenced by a product is deleted, the database will raise a foreign key constraint violation error, preventing invalid relationships. Thats all..




