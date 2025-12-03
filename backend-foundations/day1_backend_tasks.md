# 📝 BACKEND TASKS

## ✔ Easy

 Write “What is an API?” in your own words

 Ans : 
 
 API is a way to communicate between two systems. for example : Clients ask for user data to server and server return it. 
 
 Request(Client ask user data) -> Server(accept the request and return the data) -> Response (Show the data to Clients)


 List the 4 primary HTTP methods

 Ans :

 GEt    - Retrieve the data
 POST   - Create the data
 PUT    - Update the data
 DELETE - Remove the data

## ✔ Medium

 Write a fake endpoint:

 def get_user(id, name):
        return {"id" : {id}, "name" : {name}}


## ✔ Hard

 Describe your future FastAPI endpoint:

 The endpoint takes the input from users, validate the inputs using pydantic, after validation, check the server for data, and return the response to users.