# 🧪 PUT /users/{id} - Update User

## 🎯 Objective
Verify that the API allows updating an existing user using a PUT request.


## 📌 Endpoint
PUT https://reqres.in/api/users/2


## 🧾 Request Body

</>JSON


{
  "name": "Basma Updated",
  "email": "basma.updated@example.com",
  "age": 25
}

📤 Actual Result

Status Code: 200 OK
Response contains updated user data
API returns updatedAt timestamp
Metadata is included in response


📸 Evidence

[View Screenshot] ()

✅ Expected Result vs Actual Result

Expected Result	                        Actual Result
User data updated	                     ✔️ Data returned as updated
Status code 200	                       ✔️ 200 OK received
No validation errors	                 ✔️ No errors


⚠️ Notes

This API is a mock service (ReqRes).
Updates are simulated and not persisted in a real database.


🧠 Conclusion

The PUT request works as expected and correctly handles full user updates.










