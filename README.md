# Week 6 Summary

## Overview
This project is a small backend for an e-commerce application built during Week 6. It uses **Node.js**, **Express**, and **MongoDB (Mongoose)** to manage users, products, and a basic shopping cart.

## What I completed in Week 6

### 1. Backend server setup
- Created an Express server in `server.js`
- Connected the app to MongoDB using Mongoose
- Added middleware for JSON request handling
- Added basic error handling

### 2. Product API
- Added routes to create products
- Product data is stored in the `product` collection
- Product schema includes:
  - `productName`
  - `price`
  - `brand`

### 3. User API
- Added routes to create users
- Passwords are hashed using `bcryptjs` before saving
- Added a route to add a product to a user's cart
- Added a route to fetch a user by ID

### 4. Data models
- Created `ProductModel.js` for product documents
- Created `UserModel.js` for user documents
- Added a cart schema with product references and quantity tracking

### 5. API testing
- Added request examples in `ecom.http` for:
  - creating a product
  - creating a user
  - adding a product to a user's cart
  - fetching a user

## Project structure

- `server.js` - main server and MongoDB connection
- `API/userAPI.js` - user-related routes
- `API/prodAPI.js` - product-related routes
- `model/UserModel.js` - user schema and model
- `model/ProductModel.js` - product schema and model
- `ecom.http` - sample HTTP requests for testing

## How to run

1. Install dependencies
   ```bash
   npm install
   ```

2. Start MongoDB locally
   - Make sure MongoDB is running on `mongodb://localhost:27017`

3. Start the server
   ```bash
   npm start
   ```

4. The server will run on
   ```bash
   http://localhost:4000
   ```

## Main endpoints

- `POST /product-api/products`
- `POST /user-api/users`
- `PUT /user-api/user-cart/user-id/:uid/product-id/:pid`
- `GET /user-api/users/:uid`

## Notes

This Week 6 work focuses on building the core backend for an e-commerce app, including user registration, secured password storage, product creation, and cart updates.
