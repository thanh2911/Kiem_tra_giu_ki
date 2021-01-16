# Kiem_tra_giu_ki

* 1.Stop and remove old container: docker stop flask-backend && docker rm flask-backend
* 2.Build image: docker build -t backend .
* 3.Run the container: docker run -d --name flask-backend -e password=postgres -p 5000:5000 backend
# API

# Get all customer
* Request
 ^ Method: GET
Endpoint: /customer/all
Params: None
Body: None
Response: [Customer]
Add a customer
Request
Method: POST
Endpoint: /customer
Body:
customer_name: string
contact_name: string
address: string
city: string
postal_code: string
country: string
Response: Message
Update a customer
Request:
Method: PUT
Endpoint: /customer/:customer_id
Body:
customer_name: string
contact_name: string
address: string
city: string
postal_code: string
country: string
Response: Message
Delete a customer
Request:
Method: DELETE
Endpoint: /customer/:customer_id
Response: message
