# 📝 BACKEND TASKS
## ✔ Easy

### Write 5 REST endpoints for a “tasks” API

GET  (read data)           - /tasks
GET  (read one data)       - /tasks/id
POST (create data)         - /tasks
PUT  (update data)         - /tasks/id
PATCH(update data partial) - /tasks/id
DELET (remove data)        - /tasks/id


### Explain why /getUsers is wrong

Because REST has already HTTP actions in URL, so bad APIs try to put actions in the url, that's wrong way, we use like /user, /order, /user/3.

## ✔ Medium

### Write a Pydantic model for User(name, age, email)

### Describe how validation works

## ✔ Hard
### Design a REST API for a TODO application:

Must include:

Tasks

Users

Categories

Define:

Endpoints

Methods

Path params

Query params

Request bodies

Response bodies