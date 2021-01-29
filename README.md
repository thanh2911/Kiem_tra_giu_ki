# Kiem_tra_giu_ki

# How to run

* (ĐỊA CHỈ IP DOCKER em Không luu nen ... khi chấm anh chỉnh hộ phần ip docker trong dockerfile... thành ip máy anh 
*  đổi máy nó đổi ip :)) ... em c ko rành phần nay lắm... trên máy em chạy ổn )

1. Stop and remove old container: ```docker stop flask-backend && docker rm flask-backend```
1. Build image: ```docker build -t backend .```
1. Run the container: ```docker run -d --name flask-backend -e password=postgres -p 5000:5000 backend```

# Entity
## ```Customer (BANG 1)```
* id: int
* customer_name: string
* contact_name: string
* address: string
* city: string
* postal_code: string
* country: string


# API
## Customer
### Get all customer
* Request
    * Method: GET
    * Endpoint: /customers/all
    * Params: None
    * Body: None
* Response: [Customer]
### Add a customer
* Request
    * Method: POST
    * Endpoint: /customers
    * Body:
        * customer_name: string
        * contact_name: string
        * address: string
        * city: string
        * postal_code: string
        * country: string
* Response: Message
### Update a customer
* Request:
    * Method: PUT
    * Endpoint: /customers/:customer_id
    * Body:
        * customer_name: string
        * contact_name: string
        * address: string
        * city: string
        * postal_code: string
        * country: string
* Response: Message

### Delete a customer
* Request:
    * Method: DELETE
    * Endpoint: /customers/:customer_id
* Response: message


*=======================================================================

# Entity
## ```Categories (BANG 2)```
* category_id: int
* category_name: string
* description: string

# API
## Categories
### Get all categories
* Request
    * Method: GET
    * Endpoint: '/categories/all'
    * Params: None
    * Body: None
* Response: [Categories]
### Add a categories
* Request
    * Method: POST
    * Endpoint: /categories
    * Body:
         * category_name: string
         * description: string

* Response: Message
### Update a categories
* Request:
    * Method: PUT
    * Endpoint: /categories/:category_id
    * Body:
         * category_name: string
         * description: string
* Response: Message

### Delete a categories
* Request:
    * Method: DELETE
    * Endpoint: /categories/:category_id
* Response: message

*=======================================================================

# Entity
## ```Employees (BANG 3)```
* employee_id: int
* lastname: string
* firstname: string
* birthdate: date
* photo: string
* notes: string



# API
## Employees
### Get all employees
* Request
    * Method: GET
    * Endpoint: /employees/all
    * Params: None
    * Body: None
* Response: [Employees]
### Add a employees
* Request
    * Method: POST
    * Endpoint: /employees
    * Body:
         * lastname: string
         * firstname: string
         * birthdate: date
         * photo: string
         * notes: string
    * Response: Message
### Update a employees
* Request:
    * Method: PUT
    * Endpoint: /employees/:employee_id
    * Body:
         * lastname: string
         * firstname: string
         * birthdate: date
         * photo: string
         * notes: string
         * Response: Message
* Response: Message

### Delete a employees
* Request:
    * Method: DELETE
    * Endpoint: /employees/:employee_id
* Response: message


*=======================================================================

# Entity
## ```OrderDetails (BANG 4)```
* orderdetail_id: int
* order_id: string
* product_id: string
* quantity: string

# API
## OrderDetails
### Get all orderdetails
* Request
    * Method: GET
    * Endpoint: /orderdetails/all
    * Params: None
    * Body: None
* Response: [OrderDetails]
### Add a orderdetails
* Request
    * Method: POST
    * Endpoint: /orderdetails
    * Body:
         * order_id: string
         * product_id: string
         * quantity: string
         * Response: Message
### Update a orderdetails
* Request:
    * Method: PUT
    * Endpoint: /orderdetails/:orderdetail_id
    * Body:
         * order_id: string
         * product_id: string
         * quantity: string
         * Response: Message
* Response: Message

### Delete a orderdetails
* Request:
    * Method: DELETE
    * Endpoint: /orderdetails/:orderdetail_id
* Response: message


*=======================================================================

# Entity
## ```Orders (BANG 5)```
* order_id: int
* customer_id: string
* employee_id: string
* orderdate: date
* shipper_id: string


# API
## Orders
### Get all orders
* Request
    * Method: GET
    * Endpoint: /orders/all
    * Params: None
    * Body: None
* Response: [orders]
### Add a orders
* Request
    * Method: POST
    * Endpoint: /orders
    * Body:
         * customer_id: string
         * employee_id: string
         * orderdate: date
         * shipper_id: string
* Response: Message
### Update a orders
* Request:
    * Method: PUT
    * Endpoint: /orders/:order_id
    * Body:
         * customer_id: string
         * employee_id: string
         * orderdate: date
         * shipper_id: string
* Response: Message

### Delete a orders
* Request:
    * Method: DELETE
    * Endpoint: /orders/:order_id
* Response: message


*=======================================================================


# Entity
## ```Products (BANG 6)```
* product_id: int
* product_name: string
* supplier_id: string
* category_id: string
* photo: unit
* price: string



# API
## Products
### Get all products
* Request
    * Method: GET
    * Endpoint: /products/all
    * Params: None
    * Body: None
* Response: [Products]
### Add a products
* Request
    * Method: POST
    * Endpoint: /products
    * Body:
         * product_name: string
         * supplier_id: string
         * category_id: string
         * photo: unit
         * price: string

     * Response: Message
### Update a products
* Request:
    * Method: PUT
    * Endpoint: /products/:product_id
    * Body:
         * product_name: string
         * supplier_id: string
         * category_id: string
         * photo: unit
         * price: string

* Response: Message

### Delete a products
* Request:
    * Method: DELETE
    * Endpoint: /products/:product_id
* Response: message


*=======================================================================


# Entity
## ```Shippers (BANG 7)```
* shipper_id: int
* shipper_name: string
* phone: string

# API
## Shippers
### Get all shippers
* Request
    * Method: GET
    * Endpoint: '/shippers/all'
    * Params: None
    * Body: None
* Response: [Shippers]
### Add a shippers
* Request
    * Method: POST
    * Endpoint: /shippers
    * Body:
         * shipper_name: string
         * phone: string

* Response: Message
### Update a shippers
* Request:
    * Method: PUT
    * Endpoint: /shippers/:shipper_id
    * Body:
         * shipper_name: string
         * phone: string
* Response: Message

### Delete a shippers
* Request:
    * Method: DELETE
    * Endpoint: /shippers/:shipper_id
* Response: message

*=======================================================================


# Entity
## ```Suppliers (BANG 8)```
* supplier_id : int
* supplier_name: string
* contact_name: string
* address: string
* city: string
* postal_code: string
* country: string
* phone: string


# API
## Suppliers
### Get all suppliers
* Request
    * Method: GET
    * Endpoint: /suppliers/all
    * Params: None
    * Body: None
* Response: [Suppliers]
### Add a suppliers
* Request
    * Method: POST
    * Endpoint: /suppliers
    * Body:
         * supplier_name: string
         * contact_name: string
         * address: string
         * city: string
         * postal_code: string
         * country: string
         * phone: string
* Response: Message
### Update a suppliers
* Request:
    * Method: PUT
    * Endpoint: /suppliers/:supplier_id 
    * Body:
         * supplier_name: string
         * contact_name: string
         * address: string
         * city: string
         * postal_code: string
         * country: string
         * phone: string
* Response: Message

### Delete a suppliers
* Request:
    * Method: DELETE
    * Endpoint: /suppliers/:supplier_id 
* Response: message

