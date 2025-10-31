# 🏠 Airbnb Clone Backend – Requirements Documentation

## 🎯 Objective
This document outlines the **technical and functional requirements** for key backend features in the Airbnb Clone project.  
It includes API specifications, validation rules, and performance considerations for selected features.

---

## 1️⃣ User Authentication

### 🔹 Description
Handles user registration, login, and authentication for both guests and hosts using JWT-based security.

### 🔹 Functional Requirements
- Users can register as **guest** or **host**.
- Login requires **email** and **password**.
- Passwords must be securely hashed before storage.
- JWT tokens are issued upon successful login for authentication.
- Invalid credentials must return appropriate error messages.

### 🔹 API Endpoints

| Method | Endpoint | Description |
|:-------|:----------|:-------------|
| **POST** | `/api/auth/register` | Register a new user |
| **POST** | `/api/auth/login` | Log in a user and return JWT |
| **GET** | `/api/auth/profile` | Retrieve user profile (JWT required) |

### 🔹 Input / Output Specification

#### 🧾 Registration Request
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "StrongPass123!",
  "role": "host"
}
