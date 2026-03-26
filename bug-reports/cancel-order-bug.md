## Bug Report – Cancel an Order

**Environment:**  
Web application – Chrome  

**Pre-conditions:**  
1. Place an order  

**Steps:**  
1. Create a cancel request with an existing order  
2. Send the request  

**Expected:**  
Order cancels successfully  

**Actual:**  
Order does not cancel; a 400 Bad Request appears  

**Severity:** High  
**Priority:** High

**Status:** Open

![cancel-order-bug](/screenshots/cancel-bug.png)
