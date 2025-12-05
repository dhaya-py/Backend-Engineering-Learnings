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

 Headers = autherization, content-type, accept, host.

 An API headers is part of the HTTP requests or response that carries additional information about the request, this information includes metadata, 
 such as content-type, authentication, and custome data for server or clients properly process the request or response.

 Body = JSON (sending structured data), form-data (file uploads), and raw text (very rare, used for webhooks)

 when you need to send the data from a client to your API, you send it as a request body.
 request body is data sent by client to your API, and response body is data your API sends to client.


## ✔ Medium

 ### Write a Python dictionary that represents a fake HTTP request:

request = {
    "method" : "GET",
    "url"    : "/user",
    "headers": "{Authorization : "bearer token"}",
    "query-params" : "{limit: 10}"
}


## ✔ Hard

 ### Describe a real FastAPI flow you will build soon:

Client → Router → Dependency → Logic → DB → ResponseModel

Let's say - My FastAPI app is now live, client uses my app then they send the request (ex : service booking), that request checks by DNS,
then my server receives it, it goes to backend and my framework router is activate, it executes the controller or functions, then check 
business logic and db queries, after that database check and verify the data (ex : if bookings are available), now get the data from database
preparing the response like if bookings are available we need to return booking success or booking slots, if bookings aren't available
we need to return booking is not available or please select the available slots, then formatting the response like we don't return the response
with full data or model for security reasons instead we return the response with success message or necessary details what they need, otherwise
we don't publish our data unnecessarily, now send the final response to client.
