
# Pydantic & API Modeling

## 🔹 1. Pydantic Models (FastAPI foundation)

Used for:

Request bodies

Response bodies

Validation

from pydantic import BaseModel

class User(BaseModel):
    name: str
    age: int
    email: str

## 🔹 2. Request Body vs Query Params vs Path Params

Path param:
/users/10

Query param:
/users?limit=5

Body:
POST /users
{
 "name": "dhaya",
 "age": 21
}

## 🔹 3. Response Models

You control what the API returns.

Example (hide password):

class UserOut(BaseModel):
    id: int
    name: str
    email: str

## 🔹 4. Error Responses

You must return proper HTTP codes:

400 → bad client request

404 → not found

422 → validation error

500 → server failure