# API Edge Case Test Results

This document contains the results of testing the **Swagger Petstore Login API** with edge cases.

---

## Collection: Login API Edge Cases

**Endpoint Tested:**
`GET https://petstore.swagger.io/v2/user/login`

---

### Test Case 1: Empty Username & Password
**Request:**  
`GET /user/login?username=&password=`

**Expected Result:**  
400 or 401 Unauthorized  

**Actual Result:**  
200 OK – mock API always returns success  

**Status:** Failed (demo API limitation)

---

### Test Case 2: Special Characters in Username/Password
**Request:**  
`GET /user/login?username=!!!@@@&password=###$$$`

**Expected Result:**  
400 or 401 Unauthorized  

**Actual Result:**  
200 OK – mock API always returns success  

**Status:** Failed (demo API limitation)

---

###  Test Case 3: Extremely Long Username
**Request:**  
`GET /user/login?username=aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa...&password=test123`

**Expected Result:**  
400, 401, or 414 (URI too long)  

**Actual Result:**  
200 OK – mock API always returns success  

**Status:** Failed (demo API limitation)

---

## Notes
- Swagger Petstore is a **demo API**, so it does not return real login failures.
- In a production system, these edge cases would likely return proper 400/401 errors.
- This demonstrates how edge case tests are designed, even if the mock API does not behave as expected.


## Lessons Learned

- While testing the login functionality of the **Swagger Petstore API**, I discovered that the endpoint was defined as a **GET request** (`GET /user/login`).  
- In real-world applications, login should be implemented as a **POST request**, with credentials included in the request body for security reasons (rather than exposed in the URL).  
- I followed the Swagger demo specification as provided, but I recognize that this approach is **not aligned with production best practices**.  
- This project helped reinforce the importance of understanding the differences between **practice/demo environments** and **real-world implementations**.  
- Moving forward, I would design login tests using **POST** with body parameters, while continuing to validate negative cases such as empty fields, special characters, and long input values.  
