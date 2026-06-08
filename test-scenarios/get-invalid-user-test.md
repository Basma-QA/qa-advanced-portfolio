# 🧪 GET Invalid User Test

## 📌 Objective

Verify that the API correctly handles requests for a non-existent user.


## 📍 Endpoint

GET https://reqres.in/api/users/999


## 🧪 Test Case

Request:

GET https://reqres.in/api/users/999


Expected:

* Status code: 404 Not Found
* No user data returned
* Response body should be empty

Actual:

* Status code: 404 Not Found
* No user data returned
* Response body is empty

Screenshot:

[View Screenshot] (https://github.com/Basma-QA/qa-advanced-portfolio/blob/main/images/screenshots-test-api/get-invalid-user.jpg)


## 📊 Conclusion

The API correctly handles requests for non-existent users.

When an invalid user ID is provided:

* The API returns 404 Not Found
* No user information is returned
* The response body is empty

This behavior is consistent with expected REST API practices.



