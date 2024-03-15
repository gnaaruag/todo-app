# Todo App

please note that since the app is hosted on a free instance it takes a little while for the instance to spin up

This is a web application built using Node.js and Express, designed to help you manage your tasks efficiently.

## Getting Started

### Prerequisites

Make sure you have Node.js and npm installed on your machine.

### Installation

1. Clone the repository using following command:

   ```
   git clone https://github.com/your-username/todo-app.git
   ```
2. Change into the project directory:

   ```
   cd todo-app
   ```
3. Install dependencies:

   ```
   npm install
   ```

4. Use npm start for starting the application on 3000 port

   ```
   npm start
   ```

5. Here a few more miscellaneous scripts you can run

   ```
   npm test # for running tests, this runs on the test database
   npm run dev # run a dev server, this runs on the development database
   ```

### Features
- User authentication using Passport.js
- Secure password storage with bcrypt
- Sequelize ORM for interacting with a PostgreSQL database
- run tests using jest

### Dependencies
- bcrypt - Password hashing library
- cheerio - HTML parsing and manipulation
- connect-ensure-login - Ensures a user is logged in
- connect-flash - Flash messages for Express
- cookie-parser - Parse cookies in Express
- csurf - CSRF token middleware
- ejs - Embedded JavaScript templates
- express - Web application framework for Node.js
- express-session - Session middleware for Express
- passport - Authentication middleware for Node.js
- passport-local - Local authentication strategy for Passport
- pg - PostgreSQL client for Node.js
- sequelize - Promise-based ORM for Node.js
- tiny-csrf - Lightweight CSRF token middleware

### Database setup
To set up the database for the Todo App, you'll need to perform the following steps

1. Install PostgreSQL:
- If you haven't installed PostgreSQL, download and install it from the official website.
- During installation, take note of the PostgreSQL username, password, and database name you choose.

2. Configure Database Connection:
- Open the config/config.json file in your Todo App project.
- Update the development configuration with your PostgreSQL credentials:
```
{
  "development": {
    "username": "your_postgresql_username",
    "password": "your_postgresql_password",
    "database": "your_database_name",
    "host": "127.0.0.1",
    "dialect": "postgres"
  }
}

# similarly enter your production and testing database details
```
3. Run migrations
- Open a terminal in your project directory.
- Run the following commands to apply the database migrations:
```
npx sequelize-cli db:migrate
```
4. Start the Application:
- After configuring the database, start your Todo App using
```
npm start
```

Remember to replace placeholders like your_postgresql_username, your_postgresql_password, and your_database_name with your actual PostgreSQL credentials. If you encounter any issues, make sure PostgreSQL is running, and your credentials are correctly configured.
