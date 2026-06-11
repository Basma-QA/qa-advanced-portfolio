# BUG-3 - API Accepts User Creation Without Required Email Field

## Summary
The API allows user creation even when the email field is missing in the request body.

## Environment
- API: ReqRes
- Endpoint: POST /api/users
- Method: POST
- Tool: Postman

## Preconditions
API is available and accessible.

## Steps to Reproduce
1. Send a POST request to `/api/users`
2. Use the following request body:

</>json

{
  "name": "Test User"
}


3.Send the request

##Expected Result

The API should reject the request with a validation error (e.g., 400 Bad Request) because the email field is required.

##Actual Result

The API returns 201 Created and creates a user even without the email field.

##Severity

Low

##Priority

Low

##Notes

ReqRes is a mock API and does not enforce required field validation. This behavior is considered a system limitation rather than a functional defect.


##Evidence

[View Screenshot] (https://github.com/Basma-QA/qa-advanced-portfolio/blob/main/images/screenshots-bugs/bug-3-api-accepts-user-creation-without-required-email-field.jpg)


