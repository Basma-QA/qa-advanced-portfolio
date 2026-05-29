# 🧪 Test Case: Get Single User API

**ID:** TC_GET_SINGLE_USER_01  
**Module:** Users API  
**Priority:** High  
**Type:** Functional Test  
**Method:** GET  


## 🎯 Objective
Verify that the API correctly returns the details of a specific user when a valid user ID is provided.


## 🔗 Endpoint
GET https://api.example.com/users/{id}

Example:
GET https://api.example.com/users/2


## 🔧 Pre-conditions
- API is available and running  
- User with the specified ID exists in the system  
- Postman is configured  
- Valid API key if required  


## 📥 Test Data

| Field  | Value |
|--------|------|
| userId | 2     |


## 🚀 Test Steps

1. Open Postman  
2. Select **GET** method  
3. Enter the request URL:
   https://api.example.com/users/2  
4. Click **Send**  
5. Check the response status code  
6. Validate the response body  


## ✅ Expected Result

- Status code: **200 OK**
- Response contains the user details
- The following fields are present:
  - id
  - name
  - email
- Data corresponds to the requested user ID


## 📤 Actual Result

- Status code: 200  
- User information is returned correctly  


## 📊 Status
✔ Passed 



## 📸 Evidence

images/Get-single-user-api-test.jpg


## ⚠️ Notes

- Response time is acceptable  
- No error messages observed  
- Data is consistent with expected output  












