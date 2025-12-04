# Day 2 - HTTP Deep Dive Notes

## Request Lifecycle
Client → DNS → Backend → Database → Backend → Client

Steps:
1. Client sends request
2. Server accepts it
3. Route matches the endpoint
4. Middleware processes request
5. Function handles logic
6. Database query happens
7. Response is created
8. Response sent back

## Headers
Used for metadata and authentication.

## Body
Common format is JSON.

## Query vs Path Params
- Query: /users?limit=10
- Path: /users/10
