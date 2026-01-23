# Next-Ecommerce

A full-stack e-commerce platform built with Next.js, Express.js, and PostgreSQL. This project features a modern, responsive design with role-based access control for users, sellers, and administrators.

## 🚀 Features

### 👤 User Features

- **User Registration & Authentication** - Secure JWT-based authentication with refresh tokens
- **Product Browsing** - Browse products by category, brand, size, and color
- **Shopping Cart** - Add/remove items with size and color selection
- **Checkout Process** - A secure and streamlined checkout system with integrated payment options and easy address management.
- **Order Management** - Track order status and history
- **Profile Management** - Update user profile and manage addresses
- **Coupon System** - Apply discount coupons during checkout

### 🏪 Seller Features

- **Product Management** - Add, edit, and manage product listings
- **Inventory Management** - Track stock levels and sales
- **Order Management** - View and process customer orders
- **Coupon Creation** - Create and manage discount coupons
- **Sales Analytics** - View sales charts and metrics
- **Dashboard** - Comprehensive seller dashboard

### 👑 Admin Features

- **User Management** - Manage user roles and permissions
- **Seller Approval** - Approve/reject seller role requests
- **System Settings** - Configure platform settings
- **Access Control** - Manage user access and permissions
- **Analytics Dashboard** - System-wide analytics and metrics


## 🏗️ Tech Stack

### Frontend

- **Next.js**
- **TypeScript**
- **Tailwind CSS**
- **Zustand**
- **Axios**
- **Stripe**
- **Shadcn**

### Backend

- **Express.js**
- **TypeScript**
- **Prisma**
- **PostgreSQL**
- **JWT**
- **bcryptjs**
- **Multer**
- **Cloudinary**
- **Stripe**


## 🔌 API Endpoints

### Authentication

- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/refresh` - Refresh access token
- `POST /api/auth/logout` - User logout
- `POST /api/auth/request` - Request seller role
- `PUT /api/auth/role/:id` - Admin role management

### Products

- `GET /api/products` - Get all products
- `GET /api/products/:id` - Get product by ID
- `POST /api/products` - Create product (Seller/Admin)
- `PUT /api/products/:id` - Update product (Seller/Admin)
- `DELETE /api/products/:id` - Delete product (Seller/Admin)

### Cart

- `GET /api/cart` - Get user cart
- `POST /api/cart/add` - Add item to cart
- `PUT /api/cart/update` - Update cart item
- `DELETE /api/cart/remove` - Remove cart item
- `DELETE /api/cart/clear` - Clear cart

### Orders

- `GET /api/order` - Get user orders
- `POST /api/order` - Create order
- `PUT /api/order/:id` - Update order status

### Address

- `GET /api/address` - Get user addresses
- `POST /api/address` - Add address
- `PUT /api/address/:id` - Update address
- `DELETE /api/address/:id` - Delete address

### Coupons

- `GET /api/coupon` - Get available coupons
- `POST /api/coupon` - Create coupon (Seller/Admin)
- `DELETE /api/coupon/:id` - Delete coupon (Seller/Admin)

### Dashboard

- `GET /api/dashboard/stats` - Get dashboard statistics
- `GET /api/dashboard/sales` - Get sales analytics

## Admin Credentials

- Mail - `admin@ecom.com`
- Pass - `admin123`

## 🚀 Installation Guide

### Prerequisites

- Node.js (v18 or higher)
- npm or yarn
- Serverless DB Connection String Like - Neon or Supebase

### 1. Clone the Repository

```bash
git clone <repository-url>
cd Next-Ecommerce
```

### 2. Backend Setup

```bash
cd server

# Install dependencies
npm install

# Generate Prisma client
npm run prisma:generate

# Run database migrations
npm run prisma:migrate

# Seed the database (optional)
npm run prisma:seed

# Start the development server
npm run dev
```

### 3. Frontend Setup

```bash
cd client

# Install dependencies
npm install

# Start the development server
npm run dev
```

### 4. Access the Application

- Frontend: http://localhost:3000
- Backend API: http://localhost:3001


## 🔧 Environment Variables

Create `.env` files in both `client/` and `server/` directories:

### Server `.env`

```env
# Database
DATABASE_URL="your_db_uri"

# JWT
JWT_SECRET="your-super-secret-jwt-key"

# CORS
CORS_ORIGIN="http://localhost:3000"

# Cloudinary (for image uploads)
CLOUDINARY_CLOUD_NAME="your-cloudinary-cloud-name"
CLOUDINARY_API_KEY="your-cloudinary-api-key"
CLOUDINARY_API_SECRET="your-cloudinary-api-secret"

# Stripe (for payments)
STRIPE_SECRET_KEY="your-stripe-secret-key"


# Server
PORT=3001
```

### Client `.env`

```env
# API
NEXT_PUBLIC_API_URL="http://localhost:3001"

#ARCJET
ARCJET_KEY="your-arcjet-key"

# Stripe
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY="your-stripe-publishable-key"
```
