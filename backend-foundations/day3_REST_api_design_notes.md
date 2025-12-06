## 🔹 1. What is REST?

A set of rules for designing APIs.

## 🔹 2. REST API Naming Conventions

 /getUsers → WRONG
 /createUser → WRONG

 /users → list or create users
 /users/{id} → get/update/delete user

## 🔹 3. HTTP Methods in REST

GET /users → Get list

POST /users → Create

GET /users/{id} → Get one

PUT /users/{id} → Update

DELETE /users/{id} → Delete

## 🔹 4. Request Validation

Before backend logic, you must validate:

type

required fields

allowed values

formats

FastAPI uses Pydantic models for this.

Example:

from pydantic import BaseModel

class User(BaseModel):
    name: str
    age: int

## 🔹 5. Proper Response Design

Never expose internal DB structure.

Example:

 {"password": "12345"} → NEVER return this
 {"id": 1, "name": "Dhaya"}