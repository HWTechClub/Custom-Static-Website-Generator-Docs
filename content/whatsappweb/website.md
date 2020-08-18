Class Website:
It stores all the data of a user’s website. It stores the following details in the corresponding varialbles:
    • First Name
    • Last name
    • Company Name
    • Logo
    • Banner
    • Logo URL
    • Banner URL
    • Description
    • Email
    • Products : Stores in the form of key-value pair , Key is the product id and value being the instance of the class product having all the details of the product.
It has the following functions:
    • Constructor() : Initiates the website object with the given company name and other details as empty strings or empty entity.
    • addProduct () : Add the given product to our products entity
    • getProduct() : Returns the product associated with the given product id from products enitity
    • getAllProduct () : Returns list of all the products of the website
    • deleteProduct () : Delete the product associated with the given product id from our ‘products’ entity.
    • SelectProduct () : Selects the product object associated with the given key 
    • getSelectedProduct() : Returns the product that is selected in the products entity
    • toJson() : Converts all the website data into json format (Key-Value Pairs)
