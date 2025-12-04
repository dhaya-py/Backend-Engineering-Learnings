# 📝 BACKEND TASKS
## ✔ Easy

 ### Write the request lifecycle in your own words

    Request Life cycle :

    Client → DNS → Server → Backend App → Database → Backend App → Response → Client

    Breakdown inside a backend:

    Client sends request

    Server receives it

    Framework routes URL (router)

    Middleware runs

    Controller/Function executes

    Business logic

    DB queries (if needed)

    Response formatting

    Response sent back

 ### Difference between headers and body

 Headers = envelope info, not the content itself. autherization, content-type, accept, host.

 Body = JSON (sending structured data), form-data (file uploads), and raw text (very rare, used for webhooks)

## ✔ Medium

 ### Write a Python dictionary that represents a fake HTTP request:

request = {
    "method": "GET",
    "url": "/users",
    "headers": {"Authorization": "Bearer token"},
    "query_params": {"limit": 10}
}

## ✔ Hard

 ### Describe a real FastAPI flow you will build soon:

Client → Router → Dependency → Logic → DB → ResponseModel
