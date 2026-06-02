# PATCH API - Negative Test Cases

## Project

QA Advanced Portfolio

## Endpoint


PATCH https://reqres.in/api/users/{id}



# Test Case 1: Empty Request Body

## Objective

Verify API behavior when a PATCH request is sent with an empty request body.

## Request

PATCH https://reqres.in/api/users/2


Request Body:

</>JSON
{}


## Expected Result

* Status Code: 400 Bad Request or 422 Unprocessable Entity
* Validation error message returned
* Resource should not be updated

## Actual Result

* Status Code: 200 OK
* Response returned only an updated timestamp
* No validation error message

Example Response:

</>JSON
{
  "updatedAt": "2026-06-02T..."
}


## Status

Failed Validation

## Observation

The API accepts an empty PATCH request and updates the resource timestamp instead of returning a validation error.

📸 Evidence:

[View Screenshot] (https://github.com/Basma-QA/qa-advanced-portfolio/blob/main/images/patch-negative-empty-body.jpg)


---

# Test Case 2: Invalid Data Type

## Objective

Verify API behavior when a field receives an invalid data type.

## Request


PATCH https://reqres.in/api/users/2


Request Body:

</>JSON
{
  "name": true
}


## Expected Result

* Status Code: 400 Bad Request or 422 Unprocessable Entity
* Validation error indicating incorrect data type

## Actual Result

* Status Code: 200 OK
* API accepted the boolean value

Example Response:

</>JSON
{
  "name": true,
  "updatedAt": "2026-06-02T..."
}


## Status

Failed Validation

## Observation

The API does not validate data types and accepts a boolean value for the name field.

📸 Evidence:

[View Screenshot] (https://github.com/Basma-QA/qa-advanced-portfolio/blob/main/images/patch-negative-invalid-data-type.jpg)

---

# Test Case 3: Non-Existing User ID

## Objective

Verify API behavior when updating a user that does not exist.

## Request


PATCH https://reqres.in/api/users/99999


Request Body:

</>JSON
{
  "name": "Basma"
}


## Expected Result

* Status Code: 404 Not Found
* Error message indicating that the user does not exist

## Actual Result

* Status Code: 200 OK
* API accepted the request and returned an update timestamp

Example Response:

</>JSON
{
  "name": "Basma",
  "updatedAt": "2026-06-02T..."
}


## Status

Failed Validation

## Observation

The API updates a non-existing resource instead of returning a Not Found error.

📸 Evidence:

[View Screenshot] (https://github.com/Basma-QA/qa-advanced-portfolio/blob/main/images/patch-negative-non-existing-user-id.jpg)

---

# Summary

| Test Case            | Expected Status | Actual Status | Result            |
| -------------------- | --------------- | ------------- | ----------------- |
| Empty Request Body   | 400 / 422       | 200           | Failed Validation |
| Invalid Data Type    | 400 / 422       | 200           | Failed Validation |
| Non-Existing User ID | 404             | 200           | Failed Validation |

## Conclusion

The PATCH endpoint accepts invalid requests without performing strict validation. Empty payloads, incorrect data types, and non-existing user IDs are processed successfully, which would not be expected in a production-grade API.
