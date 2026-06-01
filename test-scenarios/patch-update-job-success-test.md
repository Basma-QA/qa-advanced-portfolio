# 🧪 PATCH /users/{id} - Partial Update User Job

## Objective

Verify that the API allows a partial update of an existing user's job using a PATCH request.



## Endpoint

```http
PATCH https://reqres.in/api/users/2
```



## Request Body

```json
{
  "job": "QA Engineer"
}
```



## Test Steps

1. Open Postman.
2. Create a PATCH request.
3. Enter the endpoint: `https://reqres.in/api/users/2`.
4. Select **Body → raw → JSON**.
5. Add the request body.
6. Click **Send**.
7. Verify the response.



## Expected Result

* Status code is **200 OK**.
* The response contains the updated `job` field.
* The response contains the `updatedAt` timestamp.
* No validation or server errors occur.



## Actual Result

* Status code returned: **200 OK**.
* The `job` field was successfully updated to **"QA Engineer"**.
* The response included an `updatedAt` timestamp.
* No errors were returned.



## Test Evidence

Screenshot: [View Screenshot] ()


## Conclusion

The PATCH request successfully performed a partial update of the user resource. The API returned the modified field and an update timestamp, indicating that the request was processed correctly.
