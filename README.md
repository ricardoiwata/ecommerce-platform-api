# 🛒 Mini E-commerce

> Full-stack e-commerce application with authentication, product management, shopping cart, and AWS S3 integration.

This project is a complete mini e-commerce platform built to demonstrate real-world full-stack development skills, including authentication, REST APIs, cloud storage, and modern frontend architecture.

---

## 🌎 About the Project

This application was originally developed as a technical challenge and later improved into a portfolio project, focusing on scalability, clean architecture, and production-ready features.

---

## 📂 Project Structure

/backend   → API (Node.js, Express, Sequelize, SQLite)
/frontend  → SPA (React, Vite, TypeScript)

---

## 🚀 Features

### 🔐 Authentication
- User registration and login
- JWT-based authentication
- Protected routes

### 🛍️ Products
- Paginated product listing
- Search by name or code
- Product image upload via AWS S3

### 🛒 Shopping Cart
- Add products to cart
- Update quantities
- Remove items
- Cart total calculation

### ☁️ Cloud Integration
- Secure image upload using AWS S3 pre-signed URLs

---

## 🛠️ Tech Stack

### Backend
- Node.js
- Express
- Sequelize
- SQLite
- JWT
- bcrypt
- express-validator

### Frontend
- React
- Vite
- TypeScript

### Cloud
- AWS S3 (pre-signed upload URLs)

---

## 📦 Getting Started

### Prerequisites
- Node.js (LTS)
- npm or yarn

---

### 🔧 Backend Setup

cd backend
npm install

Create a .env file:

PORT=4000
JWT_SECRET=yourSecret
CORS_ORIGIN=http://localhost:5173

AWS_ACCESS_KEY_ID=yourKey
AWS_SECRET_ACCESS_KEY=yourSecret
AWS_REGION=us-east-1
S3_BUCKET=your-bucket
S3_PUBLIC_BASE=https://your-bucket.s3.amazonaws.com

Run migrations and seeders:

npm run db:migrate
npm run db:seed

Start server:

npm run dev

API runs at: http://localhost:4000/api

---

### 💻 Frontend Setup

cd frontend
npm install

Create .env:

VITE_API_URL=http://localhost:4000/api

Run app:

npm run dev

App runs at: http://localhost:5173

---

## 🔌 API Overview

### Auth
POST /api/auth/register  
POST /api/auth/login  

### Products
GET /api/products  
GET /api/products/search  

### Cart (JWT required)
GET /api/cart  
POST /api/cart  
PUT /api/cart/:id  
DELETE /api/cart/:id  

### AWS S3
POST /api/products/:id/image/sign  
PATCH /api/products/:id/image  

---

## 🔒 Technical Highlights

- JWT authentication & middleware
- Input validation with express-validator
- Password hashing with bcrypt
- Centralized error handling
- Standardized API responses
- CORS configuration via environment variables
- AWS S3 integration with pre-signed URLs

---

## 📌 Notes

This project focuses on simulating a real-world e-commerce flow, including authentication, product browsing, and cart management.

---

👨‍💻 Built by Ricardo Silva
