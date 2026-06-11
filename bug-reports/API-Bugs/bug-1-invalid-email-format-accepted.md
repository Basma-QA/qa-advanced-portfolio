# BUG-1 - API Accepts Invalid Email Format During User Creation

## Summary

The API accepts an invalid email format and successfully creates a user instead of returning a validation error.

## Environment

* API: ReqRes
* Endpoint: POST /api/users
* Tool: Postman

## Preconditions

The API is available and accessible.

## Steps to Reproduce

1. Send a POST request to `/api/users`
2. Use the following request body:

</>json
{
  "name": "Invalid User",
  "email": "user@com"
}


3. Submit the request.

## Expected Result

The API should reject the request and return a validation error indicating that the email format is invalid.

## Actual Result

The API accepts the request and creates the user successfully with status code `201 Created`.

## Severity

Medium

## Priority

Low

## Status

Open

## Notes

ReqRes is a mock API and does not enforce strict email validation. This issue is documented as an observed behavior and data validation limitation.

## Evidence

[View Screenshot] (https://github.com/Basma-QA/qa-advanced-portfolio/blob/main/images/screenshots-bugs/bug-1-invalid-email-format-accepted.jpg)
