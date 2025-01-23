E-commerce API
This is a Node.js-based E-commerce API that handles user authentication, product management, review systems, and order management. The API includes features like JWT-based authentication, role-based access control, and more.

Table of Contents
Project Setup
Features
API Endpoints
Technologies Used
Environment Variables
Testing
Deployment
Contributors
Project Setup
Prerequisites
Node.js
MongoDB
Postman (for testing the API)
Installation
Clone the repository:

bash
Copy
Edit
git clone https://github.com/your-username/ecommerce-api-nodejs.git
cd ecommerce-api-nodejs
Install dependencies:

bash
Copy
Edit
npm install
Set up environment variables in a .env file:

plaintext
Copy
Edit
MONGO_URL=<your_mongodb_connection_string>
JWT_SECRET=<your_jwt_secret>
JWT_LIFETIME=1d
Start the server:

bash
Copy
Edit
npm start
Navigate to http://localhost:5000 to use the API.

Features
User Authentication (Register, Login, Logout)
Role-Based Access Control (Admin, User)
Product CRUD (Create, Read, Update, Delete)
Reviews System for Products
Orders Management (Create, Update, Get Orders)
JWT Authentication with Cookies
Secure API using various security middleware (helmet, xss-clean, etc.)
API Endpoints
User Authentication
POST /api/v1/auth/register – Register a new user
POST /api/v1/auth/login – Login a user
GET /api/v1/auth/logout – Logout a user
Products
GET /api/v1/products – Get all products
POST /api/v1/products – Create a new product (Admin only)
GET /api/v1/products/:id – Get single product by ID
Orders
POST /api/v1/orders – Create a new order
GET /api/v1/orders/:id – Get a single order by ID
GET /api/v1/orders/showAllMyOrders – Get all orders for the current user
... (Add more endpoints as needed)

Technologies Used
Node.js with Express.js for backend API development
MongoDB with Mongoose for database
JWT for user authentication
Bcrypt for password hashing
Helmet, xss-clean, express-rate-limit for security
Postman for API testing
Environment Variables
Ensure you have the following environment variables set in your .env file:

MONGO_URL: MongoDB connection string
JWT_SECRET: Secret key for JWT
JWT_LIFETIME: JWT token expiration duration (e.g., 1d)
Testing
You can use Postman to test the API endpoints. Here's the Postman Collection for testing all available endpoints.

Deployment
The app is deployed on Render.

To deploy the app on a platform like Heroku:

Install the Heroku CLI
Run heroku create
Push the code to Heroku using git push heroku main
Set up environment variables in the Heroku dashboard
Contributors
Your Name
