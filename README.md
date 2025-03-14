
## Group-Project-8
MIST 4610

## Team Name: 
71552 Group 8

## Team Members:
1.Alt, Jared [@jaralt](https://github.com/jaralt/Mist4610Group8)

2.Cheetha Rajesh, Sai [@saicheetha](https://github.com/saicheetha/MIST4610)

3.Gregg, Stephen [@SGREGG-4](https://github.com/SGREGG-4/Group-Project-8)

4.Lutz, Nic [@niclutz3](https://github.com/niclutz3/Supply-Chain-Database-Project)

5.Tanti, Dev [@DevTanti](https://github.com/DevTanti/Group-Project-8.git)

## Problem Description:
When it comes to supply chain management there are a lot of products that are constantly being manufactured, stored in warehouses, ordered, shipped, and delivered. Suppliers, manufacturers, warehouse managers, shipping services, and retailers need to stay constantly informed on where everything is currently and what to do to ensure everything runs smoothly. This is all extremely difficult to track without a database that can keep everyone involved informed. Without it, products may be lost, overproduced, delivered at the wrong time, shipped to the wrong location, and not evenly distributed. This could lead to millions lost for all parties involved

## Data Model:
This data model represents a supply chain system, tracking suppliers, manufacturers, products, storage, orders, and shipments. The Suppliers entity stores information about vendors providing raw materials or goods, which are recorded in the Supply_Transaction entity that links suppliers to manufacturers and logs supplied items and quantities. The Manufacturers entity details companies that produce goods, which are then stored as Products with attributes such as type, description, and manufacture date.

Inventory management is handled through the Product_Storage entity, which associates products with warehouses and tracks stock levels. Warehouses are represented in the Warehouse entity, storing details like location, capacity, and address. The Orders entity logs customer purchases, detailing order items, quantities, and buyers. Order fulfillment is tracked in Shipments, linking orders to deliveries, shipment services, and shipping speeds. Finally, Shipment_Packing records the packaging process, associating shipments with warehouses and specifying the packed items and their quantities. The relationships between these entities ensure efficient management of procurement, production, storage, and distribution.

Suppliers and Manufactures are a many to many relationship because a manufacturer can pull from many suppliers and a supplier can supply many manufacturers.

Manufacturers to product is an identifying one to many relationship because a manufacturer can make many products but a product can only have one manufacturer, products can also only exist because of the manufacturer.

Products and Warehouse have a many to many relationships because one type of product can be stored in many different warehouses and one warehouse can store many types of products.

Warehouse and Shipments have a Many to Many relationship because a Shipment can pull from many warehouses and a warehouse can put together many shipments.

Shipments and orders are a one-to-many identifying relationship because an order can be associated with many shipments, but a shipment can only be associated with one order. 

![image](https://github.com/user-attachments/assets/e10f7fec-b763-43f1-a03d-b6cf0ace630f)


## Data Dictionary:

![image](https://github.com/user-attachments/assets/6eae8503-f59f-496b-bf39-eaa7a13f8153)
![image](https://github.com/user-attachments/assets/fb4163da-b47e-4720-9768-ca0fd910ff99)
![image](https://github.com/user-attachments/assets/60160a18-a8a7-4ca5-919b-d80d5476660c)
![image](https://github.com/user-attachments/assets/a80ceca3-ff44-47bf-8a4a-0f0632409247)
![image](https://github.com/user-attachments/assets/f94dc6ee-094b-4c25-b4cc-47423802bc0f)
![image](https://github.com/user-attachments/assets/aaca4b49-143f-4406-b81a-fae49fb643ac)
![image](https://github.com/user-attachments/assets/70fae505-14ab-4214-9fba-5c3be9b59794)
![image](https://github.com/user-attachments/assets/bda886b1-ed80-4bf6-8d29-18eb67f75911)
![image](https://github.com/user-attachments/assets/140072ed-7301-4d3a-ba46-e6c60bdd408a)

## Queries:

1. This query gets the total number of orders and the total number of items shipped per product type.

![image](https://github.com/user-attachments/assets/a31a550e-e4f8-4351-9e62-71aedf77654c)
![image](https://github.com/user-attachments/assets/24d3cecf-ede7-4c94-aed6-4420e9ed6b4a)

This query is useful to see what items are selling the fastest. This is important because this business would likely need to do more frequent orders of Ram or Motherboards to keep supply up than something like Wireless Adapters. 

2. This query provides shipping details for all orders available

![image](https://github.com/user-attachments/assets/f2e5f590-cd08-4822-ac60-806d22659d75)
![image](https://github.com/user-attachments/assets/5629a27c-74c8-4ff6-bfa1-f4f6d8c337bc)

Retrieves shipment details for each order - Useful for tracking a shipment and understanding the different entities within an order such as speed, location, shipping service, and quantity. Ensures businesses can track their orders and helps identify trends within the shipment information for each order.

3. This query provides a manager with a list of products that are running low in stock

![image](https://github.com/user-attachments/assets/af9225f9-fce6-48d2-9618-614ecfff20a5)
![image](https://github.com/user-attachments/assets/0b667c7a-aba6-48d1-9adf-b6721f36622f)

By identifying low-stock items before they run out, the manager can take action to replenish inventory. Consistently low stock levels for certain products might indicate problems with suppliers, manufacturing, or distribution. The manager can investigate these potential bottlenecks and take corrective action.

4. A shipping service needs to see which warehouses contain the products needed in order to fulfill shipment #20 

![image](https://github.com/user-attachments/assets/866533ed-ea9d-4def-be83-cbfffd61e529)

This query joined the product, product storage, warehouse, and shipment packing tables to display which warehouses contain the products that the shipping service needs to stop by to get everything needed for shipment #20. This is important because a shipping service needs to be properly informed on which warehouses the need to pick products up from. This will allow them to be able to plan accordingly and assign certain drivers to certain warehouses. 

5. This query  lists  warehouses and the percentage of their total capacity that is currently used

![image](https://github.com/user-attachments/assets/81a49d1d-821b-4ce4-9fa6-67654d518de1)

We use this query to figure out what the best way to have our inventory optimized. We can see what warehouse units can have more products stored. If a warehouse has too much inventory we can have it allocated to a different unit to help with inventory management and reduce storage costs.  

6. Find the orders placed in February of 2024.

![image](https://github.com/user-attachments/assets/1224ba36-692c-412f-af1c-b3e81fe318d8)

This query shows what products are being sold in the month of February in the year 2024. Some manufacturers create monthly sheets of their orders for tax purposes and also companies can review this documentation to see what products sell the best during the month of February.

7. This query finds which warehouses have a total stock quantity greater than the average stock quantity across all warehouses.

![image](https://github.com/user-attachments/assets/859d655e-e294-4d1d-8236-535b7f843f7c)


This is useful when manufacturers need to see which warehouses are already storing a heavy amount of products and which warehouses have more excess capacity to store more products.

8: Get warehouse details where a specific product is located

![image](https://github.com/user-attachments/assets/8b272a8c-1a9e-48fb-9f74-776e1be5619d)

This helps in finding out where a specific product is located in order to understand where products are spaced out and how fast they are being sold.

9. Get details about where each product was stored and which warehouses.

![image](https://github.com/user-attachments/assets/47dac667-478a-41e6-a306-9c4eb67a7dd6)

Helps to see the total distribution of products across warehouses.

10. This query finds who manufactured each product

![image](https://github.com/user-attachments/assets/2c957aa0-75a7-4421-ae18-873b1c98a530)


Useful when trying to see where each product came from and potentially contacting manufacturers about any known defects in a specific product.



## Database information:

![image](https://github.com/user-attachments/assets/92325abf-6f99-456c-9ef3-75c27d037801)

(Queries 6,7,8, and 9 are simple queries. That's why there are no x's.)
