# Tour Management API

A RESTful API for managing tours, reviews, and users built with **Express** and **MongoDB**. The API supports authentication, CRUD operations for tours and reviews, and user management, including password resets and role-based access control.

## Features

- **User Authentication**: Sign up, login, and password management.
- **Role-Based Access**: Different levels of user roles (admin, guide, user).
- **Tours**: CRUD operations for managing tours with features like top tours, tour statistics, and distance calculations.
- **Reviews**: Create, read, update, and delete reviews for tours.
- **Geo-location**: Filter and sort tours by distance from a specified point.

## Table of Contents

1. [Installation](#installation)
2. [API Endpoints](#api-endpoints)
    - [Authentication](#authentication)
    - [User Routes](#user-routes)
    - [Tour Routes](#tour-routes)
    - [Review Routes](#review-routes)
3. [Running the App Locally](#running-the-app-locally)
4. [Technologies](#technologies)
5. [Environment Variables](#environment-variables)
6. [License](#license)

## Installation

### Prerequisites

- **Node.js** (v14 or higher)
- **MongoDB** (either local or cloud)
- **Mailtrap** (optional for email functionality)

### Steps to Install

1. **Clone the repository**:
   Open your terminal and run the following command to clone the repository:
   ```bash
   git clone https://github.com/paularinzee/Tourista.git

2. **Navigate into the project directory**:
    ```bash
    cd Tourista

3. **Install the dependencies**: 
    ```bash
    npm install

4. **Set up the environment variables: Copy the .env.example file to .env**:
    ```bash
    cp .env.example .env

5. **Run the application**:
    ```bash
    npm start

6. **Verify the API is running**: You can test the API using tools like Postman or Insomnia to make sure it's up and running. Try accessing http://localhost:3000 to verify.

## API Endpoints

### Authentication
- **POST** /signup - Register a new user
- **POST** /login - Login and get a JWT token
- **POST** /forgotPassword - Request a password reset
- **PATCH** /resetPassword/:token - Reset the password with the reset token
- **User** Routes
- **GET** /me - Get the logged-in user's details
- **PATCH** /updateMe - Update the user's details (except password)
- **DELETE** /deleteMe - Delete the logged-in user
- **GET** /users - Get all users (admin only)
- **GET** /users/:id - Get user by ID (admin only)
- **PATCH** /users/:id - Update user by ID (admin only)
- **DELETE** /users/:id - Delete user by ID (admin only)
### Tour Routes
- **GET** /top-5-cheap - Get top 5 cheapest tours
- **GET** /tour-stats - Get tour statistics
- **POST** / - Create a new tour
- **GET** /distances/:latlng/unit/:unit - Calculate the distance from a point to the tours
- **GET** /tours-within/:distance/center/:latlng/unit/:unit - Get tours within a given distance of a point
- **GET** /tours/:id - Get a single tour by ID
- **PATCH** /tours/:id - Update a tour by ID
- **DELETE** /tours/:id - Delete a tour by ID
### Review Routes
- **GET** /reviews - Get all reviews for a tour
- **POST** /reviews - Create a new review for a tour
- **PATCH** /reviews/:id - Update a review
- **DELETE** /reviews/:id - Delete a review


## Running the App Locally
To run the app locally, follow the installation steps above. You can use tools like Postman or Insomnia to test the API endpoints.

## Technologies
- **Node.js** - JavaScript runtime
- **Express** - Web framework for Node.js
- **MongoDB** - NoSQL database for storing data
- **JWT (JSON Web Token)** - Authentication mechanism
- **MailTrap** (optional) - Email service for sending emails (e.g., for password reset)


## Environment Variables
The application requires the following environment variables:

- JWT_SECRET: Secret key for signing JWT tokens
- JWT_EXPIRES_IN**: Expiration time for JWT tokens (e.g., "1h")
- JWT_COOKIE_EXPIRES_IN: Expiration time for JWT cookie in days
- SENDGRID_API_KEY: API key for SendGrid (optional)
- MONGO_URI: MongoDB connection URI