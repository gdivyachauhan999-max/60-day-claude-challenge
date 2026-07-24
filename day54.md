# Day 54 - PrepAI Capstone | Core Feature Implementation & Authentication

## Objective

The objective of Day 54 was to begin feature development for the PrepAI Capstone Project by implementing the core authentication functionality defined in Day 4 of the 10-Day Blueprint.

The primary focus was on building the backend authentication flow, implementing user registration and login APIs, adding duplicate email validation, configuring token-based authentication, and testing the APIs using Postman.

The development process followed a milestone-based approach where each feature was implemented, tested, and verified before moving to the next milestone.

---

## Project Overview

PrepAI is an AI-powered mock interview platform that helps users practice technical interviews in Java, DSA, and Web Development through an interactive interview experience.

### Tech Stack:

**Backend:**

* Java Spring Boot
* Spring Security
* Spring Data JPA
* Maven
* JWT / Token-Based Authentication

**Frontend:**

* React.js
* Vite
* React Router DOM
* Axios

**Database:**

* PostgreSQL

**Tools:**

* Git
* GitHub
* Postman
* VS Code
* pgAdmin 4

---

## Tasks Completed

### 1. Core Authentication Implementation

Started the core feature implementation planned for Day 4 of the 10-Day Blueprint.

Implemented:

* User Registration API
* User Login API
* Duplicate Email Validation
* Authentication Token Generation
* User Authentication Flow
* Authentication-related backend components
* Added and integrated 7 new backend files

The backend was restarted after implementing the authentication functionality to ensure all changes were correctly loaded and verified.

---

### 2. User Registration API

Implemented and tested the user registration functionality.

**Endpoint:**

`POST /api/auth/register`

Successfully verified that a new user can register with:

* Name
* Email
* Password

**Result:**

`201 Created`

```json
{
  "message": "Registered successfully"
}
```

---

### 3. Duplicate Email Validation

Implemented validation to prevent multiple accounts from being registered using the same email address.

Tested the registration API again using an already registered email.

**Result:**

`409 Conflict`

```text
Email is already registered
```

The duplicate email validation worked successfully.

---

### 4. User Login API

Implemented the login functionality for registered users.

**Endpoint:**

`POST /api/auth/login`

The login API successfully validates user credentials and authenticates valid users.

The response contains:

* Authentication Token
* User Name
* User Email

**Result:**

`200 OK`

The login functionality was successfully tested using Postman.

---

## 5. API Testing with Postman

Performed complete backend authentication testing using Postman.

### Test 1 — User Registration

`POST /api/auth/register`

**Result:** `201 Created` ✅

Successfully registered a new user.

### Test 2 — Duplicate Registration

`POST /api/auth/register`

**Result:** `409 Conflict` ✅

Successfully verified duplicate email validation.

### Test 3 — User Login

`POST /api/auth/login`

**Result:** `200 OK` ✅

Successfully authenticated the registered user and received the authentication token along with user information.

---

## 6. Authentication Flow Verification

The complete backend authentication flow was successfully verified.

```text
User Registration
       ↓
Email Validation
       ↓
User Stored in Database
       ↓
User Login
       ↓
Credentials Validation
       ↓
Authentication Token Generated
       ↓
Token Returned to Client
```

---

## 7. Backend Project Structure Updates

As part of the authentication implementation, 7 new backend files were created and integrated into the existing Spring Boot project structure.

The new files support the authentication workflow and maintain a modular and scalable backend architecture.

---

## 8. Milestone-Based Development

### Milestone 1 — Backend Authentication

Completed:

* Registration API
* Duplicate Email Validation
* Login API
* Authentication Token Generation
* Backend Restart
* Postman API Testing

### Verification Status

✅ Registration tested successfully
✅ Duplicate registration tested successfully
✅ Login tested successfully
✅ Authentication response verified
✅ Backend running successfully

---

## 9. Frontend Authentication — Next Milestone

The next milestone is to implement the frontend authentication layer.

Planned features:

* Login Page
* Register Page
* AuthContext
* Authentication State Management
* Protected Routes

The frontend authentication layer will connect the React application with the backend authentication APIs and allow authenticated users to access protected areas of PrepAI.

---

## Major Technical Decisions

The major technical decisions made during Day 54 include:

* Implementing authentication using Spring Boot and Spring Security.
* Creating dedicated authentication endpoints.
* Separating registration and login functionality.
* Validating duplicate email registration.
* Using token-based authentication for authenticated sessions.
* Testing backend APIs independently using Postman.
* Following a milestone-based implementation and verification workflow.
* Maintaining a modular backend structure.

---

## Key Learnings

Learned how to implement a complete backend authentication workflow using Spring Boot.

Learned how to:

* Build registration REST APIs.
* Build login REST APIs.
* Validate duplicate user registration.
* Handle HTTP status codes such as `201 Created`, `200 OK`, and `409 Conflict`.
* Generate and return authentication tokens.
* Test REST APIs using Postman.
* Verify API responses and authentication behavior.
* Validate backend functionality before moving to frontend development.
* Follow a structured milestone-based development workflow.

---

## Deliverables Completed

* User Registration API
* User Login API
* Duplicate Email Validation
* Authentication Token Generation
* Authentication Backend Components
* 7 New Backend Files
* Backend Restart and Verification
* Postman API Testing
* Successful Registration Test
* Successful Duplicate Email Test
* Successful Login Test
* Authentication Flow Verification

---

## Testing Results

| Test Case              | Endpoint                  | Result         |
| ---------------------- | ------------------------- | -------------- |
| User Registration      | `POST /api/auth/register` | ✅ 201 Created  |
| Duplicate Registration | `POST /api/auth/register` | ✅ 409 Conflict |
| User Login             | `POST /api/auth/login`    | ✅ 200 OK       |

All three authentication tests were successfully completed and verified using Postman.

---

# 📸 Project Screenshots

The following screenshots showcase the implementation and testing progress completed during Day 54:

<img width="960" height="540" alt="Screenshot 2026-07-24 201414" src="https://github.com/user-attachments/assets/0d9b6a6b-54ca-4874-905d-b8ad2642d052" />
<img width="960" height="540" alt="Screenshot 2026-07-24 201322" src="https://github.com/user-attachments/assets/d98a71b3-9238-47bd-8206-63a4c2df9ae0" />
<img width="960" height="540" alt="Screenshot 2026-07-24 201230" src="https://github.com/user-attachments/assets/06afd5f5-8fd2-4d8a-8605-7f7873096737" />
<img width="960" height="540" alt="Screenshot 2026-07-24 195502" src="https://github.com/user-attachments/assets/9eeb8d9c-eb7a-4c1e-af9b-487b39b58c9d" />
<img width="960" height="540" alt="Screenshot 2026-07-24 193543" src="https://github.com/user-attachments/assets/0377bd27-24d6-41c3-89fd-8e64eeefac7b" />
<img width="960" height="540" alt="Screenshot 2026-07-24 193406" src="https://github.com/user-attachments/assets/be818483-0ab1-4008-a9fb-3953af8f7ffd" />
<img width="960" height="540" alt="Screenshot 2026-07-24 201851" src="https://github.com/user-attachments/assets/574e29e2-8326-4583-8199-af0e8cfa64ac" />
<img width="960" height="540" alt="Screenshot 2026-07-24 201542" src="https://github.com/user-attachments/assets/ca9512bb-691c-4433-a9a4-fd0bcccb9d0a" />


> **Note:** All Day 54 project screenshots have been combined into a single showcase image for easy reference. The showcase includes the Postman registration test, duplicate email validation, login response with authentication token, backend project structure, and successful backend execution.

---

## Technical Stack

### Backend:

* Java Spring Boot
* Spring Security
* Spring Data JPA
* Maven
* JWT / Token-Based Authentication

### Frontend:

* React.js
* Vite
* React Router DOM
* Axios

### Database:

* PostgreSQL

### Tools:

* Git
* GitHub
* Postman
* pgAdmin 4
* VS Code

---

## Outcome

Successfully implemented and verified the core backend authentication functionality for the PrepAI Capstone Project.

The registration, duplicate email validation, and login workflows are now working successfully and have been tested using Postman.

The backend authentication foundation is ready for integration with the React frontend.

The next step is to implement the frontend authentication layer, including Login and Register pages, AuthContext for managing authentication state, and Protected Routes for securing authenticated application screens.

Day 54 successfully moved PrepAI from the initial project foundation into active feature development and established the authentication layer required for building the complete user experience.
