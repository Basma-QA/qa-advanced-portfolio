# 📄 SQL TESTING – USER DATA VALIDATION

## 📌 Project Overview
This document presents SQL testing activities focused on validating user data retrieval, data consistency, and email validation rules in the database.

**Testing Type:** Manual SQL / Database Testing  
**Scope:** User management data validation  



## 🧪 Test 1: GET User Data Validation (User ID = 2)

### 🎯 Objective
Validate that the system correctly retrieves user data for a specific user ID.

### ⚙️ Description
This test ensures that the database returns complete and accurate user information for a valid user request.

### 📥 Input
- User ID: 2

### ✅ Expected Result
- User data is successfully retrieved
- All fields (id, name, email, etc.) are correctly returned
- Response is valid and consistent

### 📸 Evidence
[View Screenshot] (https://github.com/Basma-QA/qa-advanced-portfolio/blob/main/images/screenshots-test-sql/sql-user-data-validation-get-user-2.jpg)



## 🧪 Test 2: GET User Data Validation Result Check

### 🎯 Objective
Verify the correctness and consistency of the returned user data.

### ⚙️ Description
This test compares the retrieved data with the expected database records to ensure data integrity.

### 📥 Input
- User ID: 2

### ✅ Expected Result
- Returned data matches database records exactly
- No missing or incorrect values

### 📸 Evidence
[View Screenshot] (https://github.com/Basma-QA/qa-advanced-portfolio/blob/main/images/screenshots-test-sql/sql-user-data-validation-get-user-2-result.jpg)


# 📄 TEST SUITE – EMAIL VALIDATION (USER MANAGEMENT)

## 📌 Project Overview
This test suite validates email handling behavior during user creation and retrieval using the ReqRes API.

⚠️ Important Note:
The ReqRes API is a mock API and does NOT enforce strict email validation rules. Therefore, even invalid email formats are accepted as valid requests. This behavior is documented as system behavior, not a defect.

**Testing Type:** API / Data Validation Testing  
**Scope:** Email handling during user creation and retrieval  
**API Used:** ReqRes (https://reqres.in)



# 🧪 EMAIL VALIDATION TEST CASES



## 🧪 Test 3.1: Valid User Creation (POST)

### 🎯 Objective
Verify that a user can be successfully created using a valid email format.

### ⚙️ Description
This test ensures that the API correctly processes valid user creation requests and stores user data properly.

### 📥 Request
</>json id="r8p1qz"
POST /api/users

{
  "name": "Test User",
  "email": "user@example.com"
}

✅ Expected Result

User is created successfully

Response contains user ID and creation timestamp

Email is accepted and returned correctly

📸 Evidence

[View Screenshot] (https://github.com/Basma-QA/qa-advanced-portfolio/blob/main/images/screenshots-test-sql/test-3-email-validation/valid-user-post.jpg)


🧪 Test 3.2: Valid User Retrieval (GET)

🎯 Objective

Verify that a created user can be retrieved successfully.

⚙️ Description

This test ensures that stored user data can be fetched correctly from the system.

📥 Request

GET /api/users/2

✅ Expected Result

User data is returned successfully

All fields are consistent and complete

No data corruption or missing values


📸 Evidence

[View Screenshot] (https://github.com/Basma-QA/qa-advanced-portfolio/blob/main/images/screenshots-test-sql/test-3-email-validation/valid-user-get.jpg)


🧪 Test 3.3: Invalid Email Validation (Negative Test – System Behavior)

🎯 Objective

Observe system behavior when submitting an invalid email format during user creation.

⚙️ Description

This is a negative test case used to evaluate how the system handles incorrect email formats during user creation.

⚠️ Important:

ReqRes API does NOT validate email format strictly. Therefore, invalid emails are accepted and processed normally.


📥 Request

POST /api/users

{
  "name": "Invalid User",
  "email": "user@com"
}

❌ Expected Behavior (Ideal System Design)

System should reject invalid email format

OR return a validation error (400 Bad Request)

📌 Actual Behavior (ReqRes API)

Request is accepted successfully

User is created despite invalid email format

No validation error is returned


📸 Evidence

[View Screenshot] (https://github.com/Basma-QA/qa-advanced-portfolio/blob/main/images/screenshots-test-sql/test-3-email-validation/invalid-email-user-created.jpg)

# 📊 FINAL CONCLUSION

This email validation test suite demonstrates:

✔ Successful user creation with valid email format 

✔ Correct retrieval of user data from the system 

✔ System behavior when handling invalid email inputs 

✔ Understanding of expected vs actual behavior in API testing 

✔ Ability to identify API limitations (mock service behavior)



# 🛠️ QA INSIGHT

- ReqRes is a mock API with simplified validation rules
  
- Email format validation is not enforced on the server side
  
- Negative test cases are still valuable to document system behavior and API limitations
  
- A strong QA approach focuses on analyzing behavior, not only detecting defects

