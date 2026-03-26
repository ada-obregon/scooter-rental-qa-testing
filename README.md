# QA Test Documentation – Scooter Rental Web Application
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


## Test Environment
| Item             | Value                     |
| ---------------- | ------------------------- |
| Application Type | Web Application           |
| Domain           | Scooter Rental / Delivery |
| Testing Type     | Manual Testing            |
| Design Reference | Figma                     |
| Main Roles       | Customer, Courier         |
| Platforms        | Desktop Browser           |


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


## Test Cases – Order Form (Customer Information)
Feature: Place Order – User Information Form
| Test Case ID | Test Scenario                      | Steps                                        | Expected Result                                                        |
| ------------ | ---------------------------------- | -------------------------------------------- | ---------------------------------------------------------------------- |
| TC-01        | Verify order form fields           | Open **Place Order** page                    | Fields displayed: First Name, Last Name, Address, Metro Station, Phone |
| TC-02        | Verify required fields             | Leave fields empty and click **Next**        | User cannot proceed                                                    |
| TC-03        | Validate First Name format         | Enter invalid characters                     | Field highlighted in red with error message                            |
| TC-04        | Validate First Name length         | Enter more than 15 characters                | Error message displayed                                                |
| TC-05        | Validate First Name minimum length | Enter less than 2 characters                 | Error message displayed                                                |
| TC-06        | Validate Last Name format          | Enter invalid characters                     | Field highlighted in red                                               |
| TC-07        | Validate Address format            | Enter unsupported characters                 | Error message displayed                                                |
| TC-08        | Validate Address length            | Enter more than 50 characters                | Error message displayed                                                |
| TC-09        | Validate Phone format              | Enter letters instead of numbers             | Error message displayed                                                |
| TC-10        | Verify Next button behavior        | Fill all fields correctly and click **Next** | Rental form opens                                                      |


## Test Cases – Rental Form
Feature: Rental Configuration
| Test Case ID | Test Scenario                 | Steps                         | Expected Result                                                |
| ------------ | ----------------------------- | ----------------------------- | -------------------------------------------------------------- |
| TC-11        | Verify rental form fields     | Open rental form              | Fields displayed: Delivery Date, Rental Period, Color, Comment |
| TC-12        | Verify required fields        | Leave Delivery Date empty     | User cannot submit order                                       |
| TC-13        | Validate Delivery Date        | Select past date              | Selection not allowed                                          |
| TC-14        | Validate Rental Period        | Select values 1–7 days        | Value accepted                                                 |
| TC-15        | Validate Comment field length | Enter more than 24 characters | Error message displayed                                        |
| TC-16        | Verify optional fields        | Leave Color and Comment empty | Order submission allowed                                       |
| TC-17        | Verify Back button            | Click **Back**                | User returns to previous page                                  |
| TC-18        | Verify data persistence       | Navigate between pages        | Entered data remains saved                                     |


## Test Cases – Order Submission
Feature: Order Creation
| Test Case ID | Test Scenario                   | Steps                                        | Expected Result                        |
| ------------ | ------------------------------- | -------------------------------------------- | -------------------------------------- |
| TC-19        | Verify order submission         | Fill all required fields and click **Order** | Order is created                       |
| TC-20        | Verify order confirmation popup | Click **Order**                              | Popup appears: "Order has been placed" |
| TC-21        | Verify order number generation  | Create order                                 | Order number displayed                 |
| TC-22        | Verify status tracking button   | Click **Check Status**                       | User navigates to Order Status page    |
| TC-23        | Verify multiple orders          | Place several orders sequentially            | All orders created successfully        |


## Test Cases – Order Status Tracking
Feature: Order Status Page
| Test Case ID | Test Scenario              | Steps                            | Expected Result                |
| ------------ | -------------------------- | -------------------------------- | ------------------------------ |
| TC-24        | Open Order Status page     | Click **Order Status** in header | Order number field appears     |
| TC-25        | Check valid order number   | Enter valid order number         | Order details displayed        |
| TC-26        | Check invalid order number | Enter invalid number             | Error message displayed        |
| TC-27        | Verify order information   | Open order details               | All fields displayed correctly |
| TC-28        | Verify status timeline     | Open order status                | Current status highlighted     |


## Test Cases – Delivery Status Workflow
Feature: Delivery Progress
| Test Case ID | Test Scenario         | Steps                        | Expected Result                           |
| ------------ | --------------------- | ---------------------------- | ----------------------------------------- |
| TC-29        | Initial order status  | Place order                  | Status: "Scooter is in the warehouse"     |
| TC-30        | Courier accepts order | Courier confirms order       | Status changes to "Courier is on the way" |
| TC-31        | Delivery arrival      | Courier presses **Complete** | Status changes to "Delivery has arrived"  |
| TC-32        | Final status          | Courier confirms completion  | Status changes to "Enjoy your ride"       |


## Test Cases – Order Cancellation
Feature: Cancel Order
| Test Case ID | Test Scenario                 | Steps                        | Expected Result                  |
| ------------ | ----------------------------- | ---------------------------- | -------------------------------- |
| TC-33        | Cancel order popup            | Click **Cancel Order**       | Confirmation popup appears       |
| TC-34        | Cancel confirmation           | Click **Cancel**             | Order canceled message displayed |
| TC-35        | Return to status page         | Click **Back**               | User returns to Order Status     |
| TC-36        | Cancel restriction            | Courier already picked order | Cancel button disabled           |
| TC-37        | Verify canceled order removal | Cancel order                 | Order removed from system        |


## Test Cases – Delayed Orders
Feature: Delivery Delay Handling
| Test Case ID | Test Scenario          | Steps                | Expected Result                        |
| ------------ | ---------------------- | -------------------- | -------------------------------------- |
| TC-38        | Delayed order status   | Delay delivery       | Status changes to "Courier is delayed" |
| TC-39        | Delay message          | View delayed order   | Warning message displayed              |
| TC-40        | Delay visual indicator | Open delayed order   | Status highlighted in red              |
| TC-41        | Rental countdown       | Order delivered late | Rental countdown starts upon delivery  |


##UI Verification
Feature: Design Validation
| Test Case ID | Test Scenario     | Expected Result      |
| ------------ | ----------------- | -------------------- |
| TC-42        | Text field design | Matches Figma design |
| TC-43        | Button design     | Matches Figma design |
| TC-44        | Header design     | Matches Figma design |
| TC-45        | Page layout       | Matches Figma design |

## Testing Techniques Used

- Boundary Value Analysis
- Input Validation Testing
- UI Verification
- Functional Testing
- Negative Testing
- Workflow Testing
- Possible Future Improvements
- API testing
- Cross-browser testing
- Mobile responsiveness testing
- Manual UI tests
- Performance testing

## Author
Ada Obregón Serrano 

QA Tester | Manual Testing | Test Documentation
