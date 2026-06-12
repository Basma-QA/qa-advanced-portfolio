# ⚠️ Edge Cases Test Scenarios

## Overview

This document defines edge case test scenarios for API validation.

Edge cases focus on unusual, extreme, or unexpected inputs that may not be covered by standard test scenarios but are critical for system robustness.



## Email Edge Cases

### EC-1 - Very Short Email Format

**Example:**


a@b.c


**Objective:** Verify system behavior with minimal valid email structure.

**Expected Result:** Email should be accepted or validated based on rules.



### EC-2 - Extremely Long Email Address

**Example:**


verylongemailaddress_exceeding_normal_limits@domain.com


**Objective:** Test system limits for email length.

**Expected Result:** System should either accept valid length or reject oversized input.



### EC-3 - Double @ Symbol in Email

**Example:**


user@@domain.com


**Objective:** Verify validation of malformed email structure.

**Expected Result:** Validation error should be returned.



### EC-4 - Empty Email Field

**Example:**


""


**Objective:** Verify system behavior when email is empty.

**Expected Result:** Validation error should be returned.



### EC-5 - Null Email Value

**Example:**


null


**Objective:** Verify system behavior with null input.

**Expected Result:** Validation error or safe handling.



## Input Field Edge Cases

### EC-6 - Single Character Input

**Example:**


A


**Objective:** Verify system behavior with minimal input.



### EC-7 - Extremely Long Name Field

**Objective:** Test system handling of oversized text input.

**Expected Result:** System should validate or reject input exceeding limits.



### EC-8 - Numeric Input in Text Field

**Example:**


123456


**Objective:** Ensure text fields reject or handle numeric-only values appropriately.



### EC-9 - Special Characters Input

**Example:**


@#$%^&*()


**Objective:** Verify system behavior with special characters.



## Security Edge Cases

### EC-10 - SQL Injection Attempt

**Example:**


' OR 1=1 --


**Objective:** Verify that system safely handles malicious input.

**Expected Result:** Input should be sanitized and not executed.



### EC-11 - Script Injection Attempt

**Example:**


<script>alert(1)</script>


**Objective:** Test basic XSS protection handling.

**Expected Result:** Input should be escaped or rejected.



## API Behavior Edge Cases

### EC-12 - Empty Request Body

**Objective:** Verify system behavior when no data is sent.

**Expected Result:** Validation error or rejection.



### EC-13 - Null Payload Submission

**Objective:** Verify system behavior when payload is null.

**Expected Result:** Proper error handling.



### EC-14 - Unexpected Data Types

**Example:**

* Sending boolean instead of string
* Sending object instead of string

**Expected Result:** Validation error or type handling.



## Conclusion

Edge case testing is essential for identifying system weaknesses that are not visible in normal testing scenarios.

It helps ensure robustness, security, and stability of the API under unexpected or extreme conditions.
