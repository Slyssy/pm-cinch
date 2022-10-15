# pm-cinch

## Tables

[X] Users Table

[X] Projects Table

[X] Expenses Table

[X] Tasks Table

[X] Timesheets Table

[X] Comments Table

## Routes

### Authorization Routes

[] <Register style="font-weight: 500;font-size: 16px">Register Route <span style="color:purple; font-size: 16px">POST(/register)</span>

- The request will include the first name, last name, position, email, phone,
  payRate, username, password and userID.
- We will use Argon2 to hash the password.
- This route will post into the users table.
- Include a conditional that will check for duplicates (no duplicates allowed).

[] <span style="font-weight: 500;font-size: 16px">Login Route <span style="color:purple; font-size: 16px">POST(/login)</span>

- The request for this route will include the username and password.
- Query the database and grab the id, first name, last name, email and the
  hashed password.
- User Argon2 (verify) to compare the hashed password in the users table to
  the password that was entered.
- If the password passes, create a token and sign it using the JSON Web Token
  package.
  <br>
  <br>

## User Routes

[] <span style="font-weight: 500;font-size: 16px">Get All Users</span> <span style="color:green; font-size: 16px">GET(/users)</span>

[] <span style="font-weight: 500;font-size: 16px">Get a User by ID</span> <span style="color:green; font-size: 16px">GET(/user/:id)</span>

[] <span style="font-weight: 500;font-size: 16px">Update a User by ID</span> <span style="color:blue; font-size: 16px">PUT(/user/:id)

[] <span style="font-weight: 500;font-size: 16px">Delete a User by ID</span> <span style="color:red; font-size: 16px">DELETE(/user/:id)</span>
<br>
<br>

## Project Routes

[] <span style="font-weight: 500;font-size: 16px">Create a New Project: </span><span style="color:purple; font-size: 16px">POST(/project)</span>

[] <span style="font-weight: 500;font-size: 16px">Get All of the Projects </span><span style="color:green; font-size: 16px">GET(/projects)</span>

[] <span style="font-weight: 500;font-size: 16px">Get a Project by ID </span><span style="color:green; font-size: 16px">GET(/project/:id)</span>

[] <span style="font-weight: 500;font-size: 16px">Update a Project by ID </span><span style="color:blue; font-size: 16px">PUT(/project/:id)</span>

[] <span style="font-weight: 500;font-size: 16px">Delete a Project by ID </span><span style="color:red; font-size: 16px">DELETE(/project/:id)</span>
<br>
<br>

## Expense Routes

[] <span style="font-weight: 500;font-size: 16px">Create a New Expense: </span><span style="color:purple; font-size: 16px">POST(/expense)</span>

[] <span style="font-weight: 500;font-size: 16px">Get All of the Expenses </span><span style="color:green; font-size: 16px">GET(/expenses)</span>

[] <span style="font-weight: 500;font-size: 16px">Get an Expense by ID </span><span style="color:green; font-size: 16px">GET(/expense/:id)</span>

[] <span style="font-weight: 500;font-size: 16px">Update an Expense by ID </span><span style="color:blue; font-size: 16px">PUT(/expense/:id)</span>

[] <span style="font-weight: 500;font-size: 16px">Delete an Expense by ID
</span><span style="color:red; font-size: 16px">DELETE(/expense/:id)</span>
<br>
<br>

## Task Routes

[] <span style="font-weight: 500;font-size: 16px">Create a New Task: </span><span style="color:purple; font-size: 16px">POST(/task)</span>

[] <span style="font-weight: 500;font-size: 16px">Get All of the Tasks </span><span style="color:green; font-size: 16px">GET(/tasks)</span>

[] <span style="font-weight: 500;font-size: 16px">Get a Task by ID </span><span style="color:green; font-size: 16px">GET(/task/:id)</span>

[] <span style="font-weight: 500;font-size: 16px">Update a Task by ID </span><span style="color:blue; font-size: 16px">PUT(/task/:id)</span>

[] <span style="font-weight: 500;font-size: 16px">Delete a Task by ID </span><span style="color:red; font-size: 16px">DELETE(/task/:id)</span>
<br>
<br>

## Time Sheet Routes

[] <span style="font-weight: 500;font-size: 16px">Create a New Time Sheet Entry: </span><span style="color:purple; font-size: 16px">POST(/timesheet)</span>

[] <span style="font-weight: 500;font-size: 16px">Get All of the Time Sheet Entries </span><span style="color:green; font-size: 16px">GET(/timesheets)</span>

[] <span style="font-weight: 500;font-size: 16px">Get a Time Sheet Entry by ID </span><span style="color:green; font-size: 16px">GET(/timesheet/:id)</span>

[] <span style="font-weight: 500;font-size: 16px">Update a Time Sheet Entry by ID </span><span style="color:blue; font-size: 16px">PUT(/timesheet/:id)</span>

[] <span style="font-weight: 500;font-size: 16px">Delete a Time Sheet Entry by ID </span><span style="color:red; font-size: 16px">DELETE(/timesheet/:id)</span>
<br>
<br>

## Comments Routes

[] <span style="font-weight: 500;font-size: 16px">Create a New Comment: </span><span style="color:purple; font-size: 16px">POST(/comment)</span>

[] <span style="font-weight: 500;font-size: 16px">Get All of the Comments </span><span style="color:green; font-size: 16px">GET(/comments)</span>

[] <span style="font-weight: 500;font-size: 16px">Get a Comment by ID </span><span style="color:green; font-size: 16px">GET(/comment/:id)</span>

[] <span style="font-weight: 500;font-size: 16px">Update a Comment by ID </span><span style="color:blue; font-size: 16px">PUT(/comment/:id)</span>

[] <span style="font-weight: 500;font-size: 16px">Delete a Comment by ID </span><span style="color:red; font-size: 16px">DELETE(/comment/:id)</span>
<br>
<br>

![erd_diagram](/public/erd.png)
