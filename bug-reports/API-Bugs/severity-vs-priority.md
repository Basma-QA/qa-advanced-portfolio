# 📊 Severity vs Priority in QA Testing

## Overview

Severity and Priority are two important concepts used in software testing to classify and manage defects.

Although they are often confused, they represent different aspects of a bug.



## Severity

**Severity** refers to the technical impact of a defect on the system.

It answers the question:

> How serious is the defect?

### Common Severity Levels

| Severity | Description                             |
| -------- | --------------------------------------- |
| Critical | System crash, data loss, security issue |
| High     | Major functionality unavailable         |
| Medium   | Functionality works incorrectly         |
| Low      | Minor issue with limited impact         |



## Priority

**Priority** refers to the urgency of fixing a defect.

It answers the question:

> How quickly should the defect be fixed?

### Common Priority Levels

| Priority | Description                          |
| -------- | ------------------------------------ |
| High     | Must be fixed immediately            |
| Medium   | Should be fixed in upcoming releases |
| Low      | Can be fixed later                   |



## Practical Examples

### Example 1: Login Failure

* Severity: High
* Priority: High

Reason: Users cannot access the application.



### Example 2: Logo Misalignment

* Severity: Low
* Priority: Low

Reason: Cosmetic issue with no functional impact.



## Application to This Project

### BUG-1 - Invalid Email Format Accepted

* Severity: Medium
* Priority: Low

Reason: Invalid data is accepted, but the API used in this project (ReqRes) is a mock API and does not enforce strict validation rules.



### BUG-2 - Empty Request Body Accepted

* Severity: Medium
* Priority: Medium

Reason: User creation is allowed without providing required information.



### BUG-3 - Missing Email Field Accepted

* Severity: Medium
* Priority: Medium

Reason: User creation succeeds even when a key field is missing.



## Conclusion

Severity measures the technical impact of a defect.

Priority measures the urgency of fixing a defect.

A QA Engineer should evaluate both aspects before reporting and classifying a bug.
