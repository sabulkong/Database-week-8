# Task Manager API

## Description

This project implements a simple Task Manager CRUD API using Node.js, Express, and MySQL. It provides endpoints to create, read, update, and delete users and tasks, connecting to a MySQL database with a 1→M relationship (one user to many tasks).

## Setup and Run

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/task-manager-api.git
   cd task-manager-api
   ```

2. **Import the database schema**

   * Open MySQL and run the provided `schema.sql` file:

     ```sql
     SOURCE path/to/schema.sql;
     ```

3. **Install dependencies**

   ```bash
   npm install
   ```

4. **Configure environment variables**

   * Create a `.env` file in the project root with the following content:

     ```ini
     DB_HOST=localhost
     DB_USER=root
     DB_PASS=yourpassword
     DB_NAME=task_manager
     PORT=3000
     ```

5. **Start the server**

   ```bash
   node server.js
   ```

6. **Test the API**

   * Use Postman or cURL to interact with:

     * `POST   /users`
     * `GET    /users`
     * `PUT    /users/:id`
     * `DELETE /users/:id`
     * `POST   /tasks`
     * `GET    /tasks`
     * `GET    /tasks/:id`
     * `PUT    /tasks/:id`
     * `DELETE /tasks/:id`

## ERD

![ERD Diagram](./erd.png)

*or*

[View the ERD on Lucidchart](https://www.lucidchart.com/invitations/accept/your-diagram-link)

