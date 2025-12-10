# 📝 BACKEND TASKS
## ✔ Easy

 Create a Pydantic model for Task(title, description, status)

 from pydantic import BaseModel

 class Task(BaseModel):
    title: str
    description: str
    status: str

## ✔ Medium

 Define request and response bodies for:
 POST /tasks
 GET /tasks/{id}

 class TaskRequest(BaseModel):
    id: int
    title: str
    description: str
    status: str

{
    title: "Backend",
    description: "define pydandic model",
    status: "on going"
}

 class TaskResponse(BaseModel):
    id: int
    title: str
    status: str
{
    id: 1
    title: "Backend",
    status: "on going"
}


## ✔ Hard

Design full API spec for a “User Authentication API”:

Must include:

signup

login

logout

refresh token

Define:

endpoints

HTTP methods

request bodies

response bodies

error cases


signup :  

purpose - User create a new account
endpoint - /user/signup
HTTP method - POST (users create their accounts)
request body -  {
                    name : "dhaya",
                    email: "dhaya@gmail",
                    password: "12345"
                }
response body - {
                    id: 1,
                    name: "dhaya",
                    email:"dhaya@gmail"
                }
error cases - "user already exists", "Invalid input data"


login : 

purpose - Authenticate user and return access + refresh tokens.
endpoint - /user/login
HTTP method - POST (users access their accounts)
response body - {
                    access_token: JWT_ACCESS_TOKEN_HERE,
                    refresh_token: JWT_REFRESH_TOKEN_HERE
                }
error cases - "Invalid credentials", "user doesn't exist"


logout :

purpose - Invalidate the refresh token so user cannot generate new access tokens.
endpoint - /user/logout
HTTP method - POST (users logout their accounts)
response body - {"Logged out successfully.."}
error cases - "Invalid token", "refresh token expired"


refresh token :

purpose - Issue a new access token using the valid refresh token.
endpoint - /user/refresh-token
HTTP method - POST (get a new token)
response body - {
                    token: "NEW_TOKEN"
                }
error cases - "Invalid token", "refresh token expired"
