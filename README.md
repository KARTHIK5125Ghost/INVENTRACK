# InvenTrack

**Microservices Inventory Management System**

Enterprise-grade inventory tracking with real-time analytics, CSV exports, and interactive dashboards.

## Architecture

inventrack/
├── api-gateway/ → Port 3000 (Entry point, JWT auth, proxying)
├── auth-service/ → Port 3001 (Register, Login, JWT)
├── product-service/ → Port 3002 (Products, Categories, Cache)
├── inventory-service/ → Port 3003 (Stock, Transactions, Alerts, Cache)
├── supplier-service/ → Port 3004 (Supplier CRUD)
├── frontend/ → Port 5173 (React + Vite)
├── seed.js → Database seeder
└── package.json → Root runner

## Quick Start

### 1. Install all dependencies

cd inventrack  
npm install  
npm run install:all  

### 2. Seed the database

npm run seed  

### 3. Start all services

npm run dev  

### 4. Open the app

http://localhost:5173  

## Login Credentials

Admin → admin@inventrack.com / admin123  
Staff → staff@inventrack.com / staff123  

## Features

Auth → JWT, bcrypt, roles  
Products → CRUD, search, cache  
Inventory → stock, alerts, transactions  
Suppliers → CRUD  
Dashboard → analytics  

## API Endpoints

/api/auth  
/api/products  
/api/inventory  
/api/transactions  
/api/suppliers  

## Security

JWT, bcrypt, Helmet, CORS, Rate limiting