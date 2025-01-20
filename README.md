# E-commerce Backend

This project is a backend system for e-commerce application. It provides various functionalities to manage products, users, orders, and more.

## Features

- **User Management**: Handle user registration, login, and profiles.
- **Product Management**: Add, update, delete, and view products.
- **Order Processing**: Manage customer orders and order statuses.
- **Authentication**: Secure endpoints using authentication mechanisms.
- **Data Validation**: Ensure data integrity and validity.

## Technologies Used

- **Node.js**: JavaScript runtime environment.
- **Express.js**: Web framework for building the API.
- **MongoDB**: NoSQL database for storing data.
- **Mongoose**: ODM library for MongoDB and Node.js.
- **JWT**: JSON Web Tokens for authentication.
- **Bcrypt**: Library for hashing passwords.

## Getting Started

### Prerequisites

- **Node.js**: Ensure Node.js is installed on your system.
- **MongoDB**: Set up a MongoDB database.

### Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/BhupeshB7/advance_EcommerceBackend.git
   ```
2. **Navigate to the Project Directory**:
   ```bash
   cd advance_EcommerceBackend
   ```
3. **Install Dependencies**:
   ```bash
   npm install
   ```

### Configuration
   ```env
   PORT=3000
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   ``` 
 
The server will run on `http://localhost:3000`.

## Folder Structure

- `__tests__/` - Contains test cases for the application.
- `config/` - Configuration files.
- `controllers/` - Functions handling requests and responses.
- `middleware/` - Custom middleware functions.
- `models/` - Mongoose schemas and models.
- `routes/` - API routes.
- `utils/` - Utility functions.
- `server.js` - Entry point of the application.

## API Endpoints

- **User Routes**:
  - `POST /api/users/register` - Register a new user.
  - `POST /api/users/login` - User login.
  - `GET /api/users/profile` - Get user profile.

- **Product Routes**:
  - `GET /api/products` - Get all products.
  - `POST /api/products` - Add a new product.
  - `PUT /api/products/:id` - Update a product.
  - `DELETE /api/products/:id` - Delete a product.

- **Order Routes**:
  - `POST /api/orders` - Create a new order.
  - `GET /api/orders/:id` - Get order details.
 
