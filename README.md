# QA Test Documentation – Scooter Rental Web Application

## QA Project Summary

This project demonstrates end-to-end manual QA testing for a scooter rental web application.

Scope includes:
- Functional testing
- Form validation
- Order workflow testing
- API testing using Postman
- Bug identification and reporting

---

## Project Overview

This repository contains manual test documentation for a Scooter Rental Web Application.

The project focuses on validating core user flows including:
- Placing an order
- Completing the rental form
- Tracking order status
- Canceling orders
- Courier delivery workflow
- Input validation
- UI consistency with design specifications

The test cases cover functional testing, UI validation, form validation, and edge cases.

---

## Testing Approach 

The testing process included:

- Requirement analysis
- Test case design using Black Box techniques
- Boundary Value Analysis and Equivalence Partitioning
- Functional and exploratory testing
- API validation using Postman
- Bug identification and reporting

---

## Bug Example  

A critical issue was identified during testing:

- Order cancellation fails with **400 Bad Request**

👉 [View Full Bug Report](bug-reports/cancel-order-bug.md)

---

## Test Artifacts 

- [Test Cases](test-cases/)
- [Checklists](manual-testing/)
- [Bug Reports](bug-reports/)
- [API Testing](api-testing/)
- [Screenshots](screenshots/)

---

## Test Environment

| Item             | Value                     |
| ---------------- | ------------------------- |
| Application Type | Web Application           |
| Domain           | Scooter Rental / Delivery |
| Testing Type     | Manual Testing            |
| Design Reference | Figma                     |
| Main Roles       | Customer, Courier         |
| Platforms        | Desktop Browser           |

---

## Main Features Tested

| Feature               | Description                                         |
| --------------------- | --------------------------------------------------- |
| Order Creation        | User submits personal data and delivery information |
| Rental Configuration  | User selects delivery date and rental period        |
| Order Status Tracking | User checks delivery progress                       |
| Order Cancellation    | User cancels order before courier pickup            |
| Courier Workflow      | Courier accepts and completes deliveries            |
| Input Validation      | Validation rules for all form fields                |
| UI Verification       | UI elements match Figma designs                     |

---

## Test Cases – Order Form (Customer Information)

**Feature:** Place Order – User Information Form

| Test Case ID | Test Scenario | Steps | Expected Result |
| ------------ | ------------ | ----- | --------------- |
| TC-01 | Verify that all order form fields are displayed correctly | Open **Place Order** page | Fields displayed: First Name, Last Name, Address, Metro Station, Phone |
| TC-02 | Verify that the system prevents submission when required fields are empty | Leave fields empty and click **Next** | User cannot proceed |
| TC-03 | Verify that the system validates First Name format | Enter invalid characters | Field highlighted in red with error message |
| TC-04 | Verify First Name maximum length validation | Enter more than 15 characters | Error message displayed |
| TC-05 | Verify First Name minimum length validation | Enter less than 2 characters | Error message displayed |
| TC-06 | Verify Last Name format validation | Enter invalid characters | Field highlighted in red |
| TC-07 | Verify Address format validation | Enter unsupported characters | Error message displayed |
| TC-08 | Verify Address maximum length validation | Enter more than 50 characters | Error message displayed |
| TC-09 | Verify Phone format validation | Enter letters instead of numbers | Error message displayed |
| TC-10 | Verify that the user can proceed with valid data | Fill all fields correctly and click **Next** | Rental form opens |

---

## Test Cases – Rental Form

**Feature:** Rental Configuration

| Test Case ID | Test Scenario | Steps | Expected Result |
| ------------ | ------------ | ----- | --------------- |
| TC-11 | Verify that all rental form fields are displayed | Open rental form | Fields displayed correctly |
| TC-12 | Verify required fields validation | Leave Delivery Date empty | User cannot submit order |
| TC-13 | Verify that past dates cannot be selected | Select past date | Selection not allowed |
| TC-14 | Verify valid rental period selection | Select values 1–7 days | Value accepted |
| TC-15 | Verify Comment field length validation | Enter more than 24 characters | Error message displayed |
| TC-16 | Verify optional fields behavior | Leave Color and Comment empty | Order submission allowed |
| TC-17 | Verify Back button navigation | Click **Back** | User returns to previous page |
| TC-18 | Verify data persistence between steps | Navigate between pages | Data remains saved |

---

## Test Cases – Order Submission

**Feature:** Order Creation

| Test Case ID | Test Scenario | Steps | Expected Result |
| ------------ | ------------ | ----- | --------------- |
| TC-19 | Verify that a user can successfully create an order | Fill all required fields and click **Order** | Order is created |
| TC-20 | Verify order confirmation popup | Click **Order** | Confirmation popup appears |
| TC-21 | Verify order number generation | Create order | Order number displayed |
| TC-22 | Verify navigation to Order Status | Click **Check Status** | User navigates to status page |
| TC-23 | Verify multiple order creation | Place several orders | All orders created successfully |

---

## UI Verification

**Feature:** Design Validation

| Test Case ID | Test Scenario | Expected Result |
| ------------ | ------------ | --------------- |
| TC-42 | Verify text field design | Matches Figma design |
| TC-43 | Verify button design | Matches Figma design |
| TC-44 | Verify header design | Matches Figma design |
| TC-45 | Verify page layout | Matches Figma design |

---

## Testing Techniques Used

- Boundary Value Analysis  
- Equivalence Partitioning  
- Functional Testing  
- Negative Testing  
- UI Verification  
- Workflow Testing  
- API Testing  

---

## Future Improvements 

- Cross-browser testing  
- Mobile responsiveness testing  
- Performance testing  
- Automation testing  

---

## Author

Ada Obregón Serrano  

QA Tester | Manual Testing | Test Documentation
