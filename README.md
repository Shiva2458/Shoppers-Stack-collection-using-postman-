# Shoppers Stack – API Testing

A Postman-based API testing project for the **Shoppers Stack** application. This collection focuses on shopper registration, authentication, and admin profile management using REST API requests.

## Project Overview

The collection contains five API requests grouped under **Admin Profile**:

| # | Request | Method | Endpoint |
|---|---|---|---|
| 1 | Register as a Shopper | `POST` | `/shopping/shoppers` |
| 2 | Shopper Login | `POST` | `/shopping/users/login` |
| 3 | Register as Admin | `POST` | `/shopping/admin` |
| 4 | Get Admin Details by ID | `GET` | `/shopping/admin/{adminId}` |
| 5 | Update Admin Details by ID | `PUT` | `/shopping/admin/{adminId}` |

**Base URL:** `https://www.shoppersstack.com`

## Tools & Technologies

- **Postman** – creating and executing API requests
- **REST API** – API communication
- **JSON** – request payload format
- **JavaScript (Postman Tests)** – response validation

## API Coverage

### 1. Shopper Registration
- Sends a `POST` request to create a shopper account.
- The sample request body includes personal and account details such as name, email, phone, gender, city, state, country, password, and zone ID.

### 2. Shopper Login
- Sends a `POST` request to authenticate a shopper.
- The sample request body includes email, password, and role.

### 3. Admin Registration
- Sends a `POST` request to create an admin profile.
- The sample request body includes profile, contact, account, status, and location fields.

### 4. Get Admin Details by ID
- Sends a `GET` request to retrieve an admin profile using an ID in the URL.
- The request uses Bearer Token authentication.
- The collection includes Postman test assertions for:
  - HTTP status code `200`
  - Response body containing the text `Rahul`
  - JSON response field `statusCode` equal to `200`
  - Response time below `2000` milliseconds

### 5. Update Admin Details by ID
- Sends a `PUT` request to update an admin profile using an ID in the URL.
- The request uses Bearer Token authentication.
- The request body contains the profile fields to be updated.

## How to Run the Collection

1. Download or clone this repository.
2. Open **Postman**.
3. Select **Import**.
4. Import the `Shoppers Stack.postman_collection.json` collection.
5. Review the request URLs and sample request bodies.
6. Replace sample account details, resource IDs, and authentication tokens with valid values for your test environment.
7. Send requests individually, or run the collection using the Postman Collection Runner.
8. Review the HTTP status, response body, and test results.

## Sample Test Validation

The collection currently contains JavaScript assertions on the **Get Admin Details by ID** request. These checks validate the response status, expected response content, JSON status field, and response time.

> Note: The collection defines these assertions, but this README does not claim that the requests have been executed successfully. Actual results depend on the API environment and valid test data.

## Repository Structure

```text
Shoppers-Stack-API-Testing/
├── README.md
└── Shoppers Stack.postman_collection.json
```

## Important Security Note

Before making this repository public:

- Remove any real email addresses, passwords, personal data, and hard-coded Bearer Tokens from the Postman collection.
- Replace sensitive values with placeholders or Postman environment variables.
- Rotate/revoke any token or credential that may have been exposed.
- Do not commit API keys, service-role keys, or other secrets to GitHub.

The uploaded collection contains hard-coded sample credentials and a Bearer Token. They have intentionally **not** been reproduced in this README. Review and sanitize the collection itself before publishing it.

## Project Scope

This repository documents API requests for shopper registration, shopper login, admin registration, retrieving admin details, and updating admin details. The supplied collection does not include saved response examples or test scripts for every request.

---

**Project:** Shoppers Stack – API Testing  
**Collection Format:** Postman Collection v2.1  
