# 🧪 Test Case: Create User API

**ID:** TC_CREATE_USER_01
**Module:** Users API
**Priority:** High
**Type:** Functional Test
**Method:** POST


## 🎯 Objective

Verify that the API successfully creates a new user when valid data is provided.


## 🔗 Endpoint

POST https://reqres.in/api/users


## 🔧 Pre-conditions

* API is available and running
* Postman is configured
* Valid API key is provided if required


## 📥 Test Data

| Field | Value       |
| ----- | ----------- |
| name  | Basma       |
| job   | QA Engineer |


## 🚀 Test Steps

1. Open Postman
2. Select **POST** method
3. Enter the endpoint URL:
   https://reqres.in/api/users
4. Navigate to **Body**
5. Select **raw** → **JSON**
6. Enter:

json
{
  "name": "Basma",
  "job": "QA Engineer"
}

7. Click **Send**
8. Verify the response


## ✅ Expected Result

* Status code is **201 Created**
* Response contains:

  * name
  * job
  * id
  * createdAt
* User is created successfully


## 📤 Actual Result

* Status code: 201 Created
* User information returned successfully
* Unique ID generated
* Creation timestamp generated


## 📊 Status

✔ Passed


## 📸 Evidence

[View Screenshot](https://github.com/Basma-QA/qa-advanced-portfolio/blob/main/images/create-user-api-test.jpg)


## ⚠️ Notes

* API returned the expected response
* User ID was generated automatically
* Creation timestamp was returned successfully


