# knauf-repo
Customer API for Fuank

This API supports the following operatios as create, update and get customer details in Salesforce and Cosmos DB.

API Spec: https://anypoint.mulesoft.com/exchange/cfe0dbcd-17c9-4189-a3e1-a66e2c3f5764/fuank-customer-api/

To run this project, 
1. Download the source from here : https://github.com/sasiknauf/knauf-repo.git
2. the run the application with below runtime or JVM argument.
 -Dencryption.key=mulesoft
 -Dmule.env=dev

Below is the curl script and test data to validate the api.
Create Customer:
curl "http://localhost:8081/api/customer" \
  -X POST \
  -d "{\r\n  \"firstName\": \"Doll\",\r\n  \"lastName\": \"Liya\",\r\n  \"companyName\": \"LiyaCorp\",\r\n  \"email\": \"info@liyacorp.com\",\r\n  \"phone\": \"98989898\",\r\n  \"address\": [\r\n    {\r\n      \"street\": \"1212111\",\r\n      \"houseNumber\": 66,\r\n      \"city\": \"Bad Homburg\",\r\n      \"country\": \"Germany\",\r\n      \"postalCode\": \"61352\"\r\n    }\r\n  ]\r\n}" \
  -H "client_id: afddfcc1709c4513898c3142aaf5e95d" \
  -H "client_secret: a3d14ad639Aa4d78a7cd5C0fE6b2a4eE" \
  -H "content-type: application/json" 

Update Customer:
curl "http://localhost:8081/api/customer" \
  -X PUT \
  -d "{\r\n  \"customerId\": \"587e0871-750e-4971-8c71-f99cfbe73749\",\r\n  \"firstName\": \"Baby\",\r\n  \"lastName\": \"Liya\",\r\n  \"companyName\": \"LiyaCorp\",\r\n  \"email\": \"info@liyacorp.com\",\r\n  \"phone\": \"98989898\",\r\n  \"address\": [\r\n    {\r\n      \"street\": \"1212\",\r\n      \"houseNumber\": 66,\r\n      \"city\": \"Bad Homburg\",\r\n      \"country\": \"Germany\",\r\n      \"postalCode\": \"61352\"\r\n    }\r\n  ]\r\n}" \
  -H "client_id: afddfcc1709c4513898c3142aaf5e95d" \
  -H "client_secret: a3d14ad639Aa4d78a7cd5C0fE6b2a4eE" \
  -H "content-type: application/json" 

Get Customer:
curl "http://localhost:8081/api/customer?customerId=587e0871-750e-4971-8c71-f99cfbe73749" \
  -H "client_id: afddfcc1709c4513898c3142aaf5e95d" \
  -H "client_secret: a3d14ad639Aa4d78a7cd5C0fE6b2a4eE" 
  
  End
