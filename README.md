# pm-cinch

## Tables

[✓] Users Table

[✓] Projects Table

[✓] Expenses Table

[✓] Tasks Table

[✓] Timesheets Table

[✓] Comments Table

![erd diagram](https://raw.githubusercontent.com/Slyssy/pm-cinch/main/public/ERD.png)

## Routes

### Authorization Routes

[✓] <Register style="font-weight: 500;font-size: 16px">Register Route <span style="color:purple; font-size: 16px">POST(/register)</span>

- The request will include the first name, last name, position, email, phone,
  payRate, username, password and userID.
- We will use Argon2 to hash the password.
- This route will post into the users table.
- Include a conditional that will check for duplicates (no duplicates allowed).

[✓] <span style="font-weight: 500;font-size: 16px">Login Route <span style="color:purple; font-size: 16px">POST(/login)</span>

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

[✓] <span style="font-weight: 500;font-size: 16px">Get All Users</span> <span
style="color:green; font-size: 16px">GET(/users)</span>

<!-- TODO: Need to figure out how to make it so only those users that are logged in can have access to all the users' information. -->

- This is an unprotected route.

- Queries the "users" table and returns the id, first name, last name, position
  of all the users.

[✓] <span style="font-weight: 500;font-size: 16px">Get a User by ID</span> <span
style="color:green; font-size: 16px">GET(/user/:id)</span>

<!-- TODO: Need to make this route accessible to only users that are logged in, but I need any user with the "Authorization Level" to be able to search for a particular user. -->

- This is an unprotected route.
- This route queries the "users" table, and it returns the id, first name, last
  name, position, email, phone, pay_rate, username and password hash for a
  particular user.

[✓] <span style="font-weight: 500;font-size: 16px">Update a User by ID</span> <span style="color:blue; font-size: 16px">PUT(/user/:id)

<!-- TODO: Need to make it so that only the logged in user can update their own route. -->

- This route makes it possible to update any field in a user's record.
- Once updated, this route returns an object of the updated user record.

[✓] <span style="font-weight: 500;font-size: 16px">Delete a User by ID</span>
<span style="color:red; font-size: 16px">DELETE(/user/:id)</span>

<!-- TODO: Need to figure out how only admin level employees can delete user records. -->

- This route deletes a record by a user ID.
- This route will send back a status of ok and confirms the number of records
  that have been deleted.
  <br>
  <br>

## Project Routes

[✓] <span style="font-weight: 500;font-size: 16px">Create a New Project: </span><span style="color:purple; font-size: 16px">POST(/project)</span>

- This is a protected route.
-

[✓] <span style="font-weight: 500;font-size: 16px">Get All of the Projects </span><span style="color:green; font-size: 16px">GET(/projects)</span>

[✓] <span style="font-weight: 500;font-size: 16px">Get a Project by ID </span><span style="color:green; font-size: 16px">GET(/project/:id)</span>

[✓] <span style="font-weight: 500;font-size: 16px">Update a Project by ID </span><span style="color:blue; font-size: 16px">PUT(/project/:id)</span>

[✓] <span style="font-weight: 500;font-size: 16px">Delete a Project by ID </span><span style="color:red; font-size: 16px">DELETE(/project/:id)</span>
<br>
<br>

## Expense Routes

[✓] <span style="font-weight: 500;font-size: 16px">Create a New Expense: </span><span style="color:purple; font-size: 16px">POST(/expense)</span>

[✓] <span style="font-weight: 500;font-size: 16px">Get All of the Expenses for a
Project</span><span style="color:green; font-size: 16px">GET(/expenses/:projectID)</span>

[✓] <span style="font-weight: 500;font-size: 16px">Get an Expense by ID </span><span style="color:green; font-size: 16px">GET(/expense/:id)</span>

[✓] <span style="font-weight: 500;font-size: 16px">Update an Expense by ID </span><span style="color:blue; font-size: 16px">PUT(/expense/:id)</span>

[✓] <span style="font-weight: 500;font-size: 16px">Delete an Expense by ID
</span><span style="color:red; font-size: 16px">DELETE(/expense/:id)</span>
<br>
<br>

## Task Routes

[✓] <span style="font-weight: 500;font-size: 16px">Create a New Task: </span><span style="color:purple; font-size: 16px">POST(/task)</span>

[✓] <span style="font-weight: 500;font-size: 16px">Get All of the Tasks for a Project</span><span style="color:green; font-size: 16px">GET(/tasks/:id)</span>

[✓] <span style="font-weight: 500;font-size: 16px">Update a Task by ID </span><span style="color:blue; font-size: 16px">PUT(/task/:id)</span>

[✓] <span style="font-weight: 500;font-size: 16px">Delete a Task by ID </span><span style="color:red; font-size: 16px">DELETE(/task/:id)</span>
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
