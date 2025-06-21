# TestAPI – REST API Testing Project (Junior QA Portfolio)

## 📌 Project Goal
To test and validate a public REST API (https://reqres.in) using Postman. This includes positive and negative test cases for user creation, login, updating, and deletion.

## 🧰 Tools Used
- Postman
- ReqRes public API
- JavaScript (for Postman test scripts)
- GitHub for project tracking

## 🔍 Test Scenarios

| Test Case ID | Description                        | Method | Endpoint                      | Expected Result |
|--------------|------------------------------------|--------|-------------------------------|------------------|
| TC001        | Get list of users                  | GET    | /api/users?page=2             | 200 + user list  |
| TC002        | Get single user                    | GET    | /api/users/2                  | 200 + user data  |
| TC003        | Create new user                    | POST   | /api/users                    | 201 + ID returned|
| TC004        | Login success                      | POST   | /api/login                    | 200 + token      |
| TC005        | Login with missing password        | POST   | /api/login                    | 400 + error msg  |
| TC006        | Update user                        | PUT    | /api/users/2                  | 200 + updated    |
| TC007        | Delete user                        | DELETE | /api/users/2                  | 204 (no content) |

## ✅ Sample Test Script (Postman)
```javascript
pm.test("Status code is 200", () => {
    pm.response.to.have.status(200);
});
