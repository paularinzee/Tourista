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

