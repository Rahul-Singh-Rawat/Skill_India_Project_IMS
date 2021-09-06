# Skill_India_Project_IMS
Project of Inventory management system in python language

Files used in project 
1. Project IMS.ipynb        (contains python program to purchase product , adding item to inventory and displaying all the customers data)
2. inventory_record.json    (stores the inventory data about different products)
3. sold_data.json           (stores the customer data and transaction data )

# File -> Project IMS.ipynb
Python is used to make project
working of code is divided in three parts details are given below:
1. purchase of product
    1. for each new customer each time a new transaction id is generated with the help of date and time function to give uniqueness to the transaction id
    2. for every new customer every time his or her name is asked and saved in the sold_data.json file 
    3. To help customer choose product , product name and product id is displayed first so that customer can choose product and input the unique product id to add product in cart and then product quantity is asked which will be checked is present in inventor or not above step is repeated until customer enter 0  for product id which means we can now generate bill
    4. Bill is the generated for all products also discount is calculated and adjusted in the final bill which is then displayed on screen.
    
2.  Adding item to the inventory(This part of program is used by employee to add product in the inventory)
    1. Current inventory data is displayed on screen
    2. Product id is then asked whose value is needed to be updated
    3. Quantity is then asked to be added in the inventory if it is greater than zero than only inventory is updated and a confirmation message is displayed.
    
3. Displaying all purchase data
    1. Just run the program to load and print the data of all the sales done which is saved in sale_data.json
    
# File -> inventory_record.json
This file contain all the inventory data about the different products present in the inventory
To make all the products unique a unique id called product_id is used
Following is object type of inventory_record.json file
```
object{ 
        p_id : {                            //unique product id
                    name	:    	    //product name
                    quantity	:	    //product quantity present in inventory
                    mrp	        :	    //MRP of the product
                    category    :           //category of product
                    discount	:           //discount to be applied on MRP
                }
       }
```

# File -> sold_data.json
This file contain all the sales made during the purchase of product 
To make all the sell data objects unique a unique id called transaction id is used which is based on date and time of purchase
Following is object type of sold_data.json file
```
object{
        tran_id : {                 //unique transaction generated at time of purchase
                     cus_name   :   //contains customer name 
                     date_time  :   //date and time of purchase
                     bill       :   //total bill amount
	             p_id   :       //a list containing all the product id purchased by the customer
	             p_qu   :       //a list containing all the respective quantities of products purchased
                   }
       }
```      
                     
                     
                     
