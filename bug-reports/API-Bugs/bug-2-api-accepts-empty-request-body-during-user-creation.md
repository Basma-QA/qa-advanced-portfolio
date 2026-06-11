# BUG-2 - API Accepts Empty Request Body During User Creation

## Summary
The API allows user creation even when the request body is empty.

## Environment
- API: ReqRes
- Endpoint: POST /api/users
- Method: POST
- Tool: Postman

## Preconditions
API is available and accessible.

## Steps to Reproduce
1. Send a POST request to `/api/users`
2. Set header: Content-Type: application/json
3. Send an empty JSON body:
</>json

{}         

##Expected Result

The API should reject the request with a validation error (e.g., 400 Bad Request) because required fields are missing.


##Actual Result

The API returns 201 Created and creates a user even with an empty request body.


##Severity

Low

##Priority

Low

##Notes

ReqRes is a mock API and does not enforce required field validation. This behavior is considered a system limitation rather than a functional defect.


##Evidence

[View Screenshot] (https://github.com/Basma-QA/qa-advanced-portfolio/blob/main/images/screenshots-bugs/bug-2-api-accepts-empty-request-body-during-user-creation.jpg)

