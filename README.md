{
  "info": {
    "_postman_id": "a9e42c40-b8c5-4d24-aed2-6bb1aa36a550",
    "name": "Dealer-Vehicle-Payment API",
  },

  "item": [
    {

    
      "name": "Dealers",
      "item": [
        {
          "name": "Create Dealer",
          "request": {
            "method": "POST",
            "header": [
              { "key": "Content-Type", "value": "application/json" }
            ],
            "body": {
              "mode": "raw",
              "raw": "{\n  \"name\": \"Alpha Motors\",\n  \"email\": \"alpha@example.com\",\n  \"subscriptionType\": \"PREMIUM\"\n}"
            },
            "url": {
              "raw": "http://localhost:8080/api/dealers",
              "protocol": "http",
              "host": ["localhost"],
              "port": "8080",
              "path": ["api", "dealers"]
            }
          }
        },
        {
          "name": "Get All Dealers",
          "request": {
            "method": "GET",
            "url": "http://localhost:8080/api/dealers"
          }
        },
        {
          "name": "Get Dealer by ID",
          "request": {
            "method": "GET",
            "url": "http://localhost:8080/api/dealers/1"
          }
        },
        {
          "name": "Update Dealer",
          "request": {
            "method": "PUT",
            "header": [
              { "key": "Content-Type", "value": "application/json" }
            ],
            "body": {
              "mode": "raw",
              "raw": "{\n  \"name\": \"Alpha Motors Pvt Ltd\",\n  \"email\": \"alpha_updated@example.com\",\n  \"subscriptionType\": \"BASIC\"\n}"
            },
            "url": "http://localhost:8080/api/dealers/1"
          }
        },
        {
          "name": "Delete Dealer",
          "request": {
            "method": "DELETE",
            "url": "http://localhost:8080/api/dealers/1"
          }
        }
      ]
    },





    
    {
      "name": "Vehicles",
      "item": [
        {
          "name": "Create Vehicle",
          "request": {
            "method": "POST",
            "header": [
              { "key": "Content-Type", "value": "application/json" }
            ],
            "body": {
              "mode": "raw",
              "raw": "{\n  \"model\": \"Model X\",\n  \"price\": 80000,\n  \"status\": \"AVAILABLE\",\n  \"dealerId\": 1\n}"
            },
            "url": "http://localhost:8080/api/vehicles"
          }
        },
        {
          "name": "Get All Vehicles",
          "request": {
            "method": "GET",
            "url": "http://localhost:8080/api/vehicles"
          }
        },
        {
          "name": "Get Vehicle by ID",
          "request": {
            "method": "GET",
            "url": "http://localhost:8080/api/vehicles/1"
          }
        },
        {
          "name": "Get Vehicles by Dealer ID",
          "request": {
            "method": "GET",
            "url": "http://localhost:8080/api/vehicles/dealer/1"
          }
        },
        {
          "name": "Get Vehicles of Premium Dealers",
          "request": {
            "method": "GET",
            "url": "http://localhost:8080/api/vehicles/premium-dealers"
          }
        },
        {
          "name": "Update Vehicle",
          "request": {
            "method": "PUT",
            "header": [
              { "key": "Content-Type", "value": "application/json" }
            ],
            "body": {
              "mode": "raw",
              "raw": "{\n  \"model\": \"Model X Updated\",\n  \"price\": 85000,\n  \"status\": \"SOLD\",\n  \"dealerId\": 1\n}"
            },
            "url": "http://localhost:8080/api/vehicles/1"
          }
        },
        {
          "name": "Delete Vehicle",
          "request": {
            "method": "DELETE",
            "url": "http://localhost:8080/api/vehicles/1"
          }
        }
      ]
    },
    {
      "name": "Payments",
      "item": [
        {
          "name": "Initiate Payment",
          "request": {
            "method": "POST",
            "header": [
              { "key": "Content-Type", "value": "application/json" }
            ],
            "body": {
              "mode": "raw",
              "raw": "{\n  \"dealerId\": 1,\n  \"amount\": 2500.0,\n  \"method\": \"UPI\"\n}"
            },
            "url": "http://localhost:8080/api/payment/initiate"
          }
        },
        {
          "name": "Get Payment by ID",
          "request": {
            "method": "GET",
            "url": "http://localhost:8080/api/payment/1"
          }
        }
      ]
    }
  ],
  "protocolProfileBehavior": {}
}
