# GET Users - Data Validation (API Testing)

## 📌 Objective
The goal of this test is to validate the integrity and quality of user data returned by the API endpoint:

https://reqres.in/api/users?page=2

We ensure that:
- The API returns a successful response
- User data structure is correct
- Email format is valid
- Data is not empty



## 🧪 Test Cases

### 1. Status Code Validation
- Ensure the API returns status code 200
- Expected result: 200 OK



### 2. Data Existence Validation
- Verify that the response contains user data
- Condition: data array length > 0
- Expected result: Users list is not empty



### 3. User Data Structure Validation
- Each user must contain:
  - id
  - email
  - first_name
  - last_name
  - avatar

- Expected result: All required fields exist



### 4. Email Format Validation
- Verify that each email follows a valid format using regex
- Expected format: name@domain.com

- Expected result: All emails are valid



## 🧪 Tools Used
- Postman
- JavaScript (Postman Tests)
- Reqres API



## 📸 Evidence
[View Screenshot] ()



## ✅ Conclusion
This test ensures basic API data quality validation and demonstrates skills in API testing, assertions, and data verification.
