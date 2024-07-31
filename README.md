
# Personal-Finance-Tracker

Personal Finance Tracker is a web application designed to help users manage their income, expenses, and savings goals. The application allows users to track their financial data, visualize income and expenses through charts and graphs, and set and monitor budgets. Admin users can manage user data within the system.

## Table of Contents

- [Financial Tracker Evolved](#financial-tracker-evolved)
  - [Table of Contents](#table-of-contents)
  - [Features](#features)
  - [Technologies](#technologies)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Routes](#routes)
    - [API Routes](#api-routes)
      - [User Routes:](#user-routes)
      - [Finance Routes:](#finance-routes)
      - [Views Routes:](#views-routes)
  - [Database Models](#database-models)
    - [User](#user)
    - [Finance Record](#finance-record)
    - [Category](#category)
  - [License](#license)
  - [Contributing](#contributing)
  - [Contributors](#contributors)
  
## Features

  -User authentication and authorization using JWT.
  -Secure handling of sensitive data.
  -Visualizations for income and expenses (charts, graphs).
  -Budget setting and tracking.
  -Responsive design and polished UI.
  -Deployed on Heroku.
  
## Technologies

  -Node.js
  -Express.js
  -MongoDB with Mongoose ODM
  -React.js
  -@apollo/server
  -JWT (JSON Web Token) for authentication
  -CSS-in-JS using styled-components

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/Vivinyu/financial-tracker-evolved.git

2. **Install dependencies for the backend:**

   ```bash
   cd server
   npm install

3. **Install dependencies for the frontend:**

   ```bash
   cd ../client
   npm install

4. **Set Up environment variables:**

   - Create a .env file in the backend directory with the following variables:

5. **Set up the database.**

   ```bash
   MONGODB_URI='mongodb://localhost:27017'
   JWT_SECRET='JWT_SECRET='your_super_secret_key_here'
'

## Usage

1. **Start the backend server:**

   ```bash
   cd backend
   npm start

2. **Start the frontend development server:**

   ```bash
   cd ../frontend
   npm start

3. **Navigate to http://localhost:3001 to use the application.**

## Routes

### API Routes

#### User Routes

- `POST /api/users/register`: Register a new user.
- `POST /api/users/login`: Log in a user.
- `POST /api/users/logout`: Log out a user.

#### Finance Routes

- `GET /api/finances`: Get all finance records for the logged-in user.
- `POST /api/finances`: Create a new finance record.
- `PUT /api/finances/:id`: Update a finance record by ID.
- `DELETE /api/finances/:id`: Delete a finance record by ID.

#### Views Routes

- `GET /: Home`: Go to the Home page.
- `GET /login`: Login page.
- `GET /register`: Registration page.
- `GET /Dashboard`: User dashboard.
- `GET /Budget`: Page to add a new finance record.

## Database Models

### User

- `id: ObjectId, Primary Key
- `username: String, Unique, Not Null
- `email: String, Unique, Not Null
- `password: String, Not Null
  
### Finance Record

- `id: ObjectId, Primary Key
- `amount: Number, Not Null
- `type: String, Not Null (Income/Expense)
- `category_id: ObjectId, Foreign Key
- `date: Date, Not Null
- `user_id: ObjectId, Foreign Key

### Category

- `id: ObjectId, Primary Key
- `name: String, Not Null

## Contributing

Contributions are welcome! Please submit a pull request or open an issue to discuss changes.

## Contributors

Name: Anna Blount
GitHub: https://github.com/silvernotshell
LinkedIn: 

Name: Jose De Los Santos Oliver
GitHub:[GitHub Profile](https://github.com/Vivinyu)
LinkedIn:www.linkedin.com/in/jose-de-los-santos-oliver-cts-ccent-280474255
