# 🧪 DELETE User Test

## 📌 Objective

Verify that the API successfully processes a DELETE request for an existing user.


## 📍 Endpoint

DELETE https://reqres.in/api/users/2


## 🧪 Test Case

Request:

```http
DELETE https://reqres.in/api/users/2
```

Expected:

* Status code: 204 No Content
* User deletion processed successfully
* Response body should be empty

Actual:

* Status code: 204 No Content
* Response body is empty

Screenshot:

[View Screenshot]()


## 📊 Conclusion

The API correctly handles DELETE requests.

When a DELETE request is sent:

* The API returns 204 No Content
* No response body is returned
* The request is processed successfully


## ⚠️ API Limitation

ReqRes is a mock API designed for testing and learning purposes.

Although the API returns a successful deletion response, it does not perform a real deletion operation in a persistent database.

Therefore, the response simulates successful behavior rather than actually removing user data.



