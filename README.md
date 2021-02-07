# Order Management Api
  Order Management Api is a Web Application  design to order various items as per customer requirement.
  
  It consists of Post Api for creating customer order :
   
   Request :
    URI  https://127.0.0.1:3306/orders
    Method : POST
    Body : 
     [
     {
     "orderId": "A100",
     "timestamp": "2021-02-07T09:39:18.58",
     "status": 0,
     "orderTotal": 10.23,
     "shippingCost": 3.45,
     "customerId": "C100",
     "itemId": "I100",
     "quantity": 1,
     "note": "test"}
     ]
     
   Response :
    Status Usage
    200 - OK order created
    400 - Bad request Request invalid
         {
          "timestamp": "2020-10-29T15:49:21.581+00:00",
          "path": "/orders",
          "status": 400,
          "error": "Bad Request",
          "message": "timestamp is in a format that is not supported",
          "requestId": "403a779d-5"}
    500 - Internal Server Error
        {
          "timestamp": "2020-10-29T15:49:21.581+00:00",
          "path": "/orders",
          "status": 500,
          "error": "Internal server error",
          "message": "Ther server encountered an internal error and was unable to complete your request",
          "requestId": "403a779d-5"
        }
