# API and UI Automation Testing Project

This project demonstrates my ability to design and execute both **UI and API test automation** using industry-standard tools.

## Project Highlights
- Built a **Cypress automation script** to test the login flow of a sample e-commerce website.
- Designed **API edge case tests** (invalid credentials, special characters, long inputs) against the Swagger Petstore API using **Postman**.
- Implemented **Postman test scripts** to validate status codes, response times, and error handling.
- Documented **test results** and **edge case scenarios** in Markdown for professional reporting.
- Published a complete project repository on GitHub, including:
  -  Postman Collection (`.json`)
  -  API Test Results (`API_Test_Results.md`)
  -  Edge Case List (`Edge_Case_List.md`)

## 🔹 Skills Demonstrated
- UI **automation testing** with Cypress  
- Writing and executing **edge case tests**  
- Using **Postman** for API validation 
- Clear documentation in **Markdown**  
- Version control with **GitHub**

## Lessons Learned

- While testing the login functionality of the **Swagger Petstore API**, I discovered that the endpoint was defined as a **GET request** (`GET /user/login`).  
- In real-world applications, login should be implemented as a **POST request**, with credentials included in the request body for security reasons (rather than exposed in the URL).  
- I followed the Swagger demo specification as provided, but I recognize that this approach is **not aligned with production best practices**.  
- This project helped reinforce the importance of understanding the differences between **practice/demo environments** and **real-world implementations**.  
- Moving forward, I would design login tests using **POST** with body parameters, while continuing to validate negative cases such as empty fields, special characters, and long input values.  

## Value
This project reflects my ability to:
- Identify meaningful **edge cases** that uncover system weaknesses.
- Use automation to improve **efficiency and consistency** in testing.
- Communicate technical results in a way that recruiters, managers, and developers can understand.

