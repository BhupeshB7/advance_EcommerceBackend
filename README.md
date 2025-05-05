# 🛒 E-Commerce Backend API

[![Node.js](https://img.shields.io/badge/Node.js-16.x-green)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-4.x-blue)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-green)](https://www.mongodb.com/cloud/atlas)
[![JWT](https://img.shields.io/badge/JWT-Authentication-orange)](https://jwt.io/)
[![Socket.io](https://img.shields.io/badge/Socket.io-4.x-black)](https://socket.io/)

A robust, scalable, and production-ready RESTful API backend for e-commerce applications with real-time features, secure authentication, and comprehensive product management.

## 🌟 Features

- **Secure Authentication System**
  - JWT-based authentication with HTTP-only cookies
  - Password hashing with bcrypt
  - Role-based access control (Admin/User)
  - Token refresh mechanism

- **Comprehensive Product Management**
  - Advanced product search with multiple filtering options
  - Product categorization with hierarchical structure
  - Dynamic attributes system for products
  - Image upload and management

- **Order Processing**
  - Complete order lifecycle management
  - Payment processing integration
  - Order status tracking
  - Sales analytics

- **User Management**
  - User profiles with address information
  - Order history tracking
  - User reviews and ratings system

- **Real-time Features**
  - Live order notifications
  - Real-time admin-customer chat
  - Socket.io integration for instant updates

- **Security Features**
  - Helmet for HTTP security headers
  - Input validation and sanitization
  - MongoDB injection protection
  - CORS configuration

## 🏗️ Architecture

This backend follows a modular architecture with clean separation of concerns:

```
project/
├── controllers/       # Business logic layer
├── models/           # Data models and schemas
├── middleware/       # Request processing middleware
├── routes/           # API endpoints routing
├── config/           # Configuration settings
├── utils/            # Helper utilities
└── __tests__/        # Test suites
```

## 💻 Technology Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB (with Mongoose ODM)
- **Authentication**: JWT (JSON Web Tokens)
- **Real-time Communication**: Socket.io
- **File Handling**: express-fileupload
- **Security**: Helmet, bcrypt
- **Testing**: Jest

## 🔧 API Endpoints

### Products

```
GET    /api/products                  - Get all products with filtering
GET    /api/products/bestsellers      - Get bestselling products
GET    /api/products/category/:name   - Get products by category
GET    /api/products/search/:query    - Search products
GET    /api/products/get-one/:id      - Get single product details
POST   /api/products/admin            - Create new product (Admin)
PUT    /api/products/admin/:id        - Update product (Admin)
DELETE /api/products/admin/:id        - Delete product (Admin)
```

### Categories

```
GET    /api/categories                - Get all categories
POST   /api/categories                - Create new category (Admin)
POST   /api/categories/attr           - Add attribute to category (Admin)
DELETE /api/categories/:category      - Delete category (Admin)
```

### Users

```
POST   /api/users/register            - Register new user
POST   /api/users/login               - Login user
PUT    /api/users/profile             - Update user profile
GET    /api/users/profile/:id         - Get user profile
POST   /api/users/review/:productId   - Add product review
GET    /api/users                     - Get all users (Admin)
PUT    /api/users/:id                 - Update user (Admin)
DELETE /api/users/:id                 - Delete user (Admin)
```

### Orders

```
GET    /api/orders                    - Get user orders
GET    /api/orders/user/:id           - Get specific order
POST   /api/orders                    - Create new order
PUT    /api/orders/paid/:id           - Mark order as paid
PUT    /api/orders/delivered/:id      - Mark order as delivered (Admin)
GET    /api/orders/admin              - Get all orders (Admin)
GET    /api/orders/analysis/:date     - Get order analytics (Admin)
```

### Authentication

```
GET    /api/logout                    - Logout user
GET    /api/get-token                 - Verify token validity
```

## 🚀 Getting Started

### Prerequisites

- Node.js (v14+)
- MongoDB instance or MongoDB Atlas account
- npm or yarn

### Environment Variables

Create a `.env` file in the root directory with the following variables:

```
NODE_ENV=development
PORT=5000
MONGO_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<dbname>
JWT_SECRET_KEY=your_jwt_secret_key
```

### Installation

1. Clone the repository
   ```
   git clone https://github.com/yourusername/ecommerce-backend.git
   cd ecommerce-backend
   ```

2. Install dependencies
   ```
   npm install
   ```

3. Start the development server
   ```
   npm run dev
   ```

4. For production
   ```
   npm run start
   ```

## 🧪 Testing

Run comprehensive tests for the API:

```
npm test
```

The test suite covers authentication, product operations, order processing, and user management.

## 📊 Database Design

The application uses MongoDB with Mongoose schemas for structured data:

- **User Schema**: User account information with address details
- **Product Schema**: Product details with dynamic attributes and reviews
- **Order Schema**: Order processing with status tracking
- **Category Schema**: Hierarchical product categorization
- **Review Schema**: User product reviews and ratings

## 🔒 Security Implementation

- **Secure Authentication**: JWT tokens stored in HTTP-only cookies
- **Password Security**: bcrypt hashing with salt for password storage
- **Input Validation**: Server-side validation for all user inputs
- **Protected Routes**: Middleware for role-based access control
- **HTTP Security**: Helmet middleware for setting security headers
- **Sanitization**: Prevention of NoSQL injection and XSS attacks

## ⚡ Performance Optimizations

- **Database Indexing**: Strategic indexes on frequently queried fields
- **Query Optimization**: Efficient MongoDB queries and population strategies
- **Pagination**: Implemented for large data sets
- **Caching**: Cache-friendly responses with appropriate headers
- **Error Handling**: Robust error management and logging

## 🌐 Deployment

This backend is designed for easy deployment to various platforms:

  
---

## 🙏 Acknowledgements

- MongoDB for database solutions
- Express.js community for the robust framework
- Socket.io for real-time capabilities
- All open-source contributors whose libraries made this project possible
