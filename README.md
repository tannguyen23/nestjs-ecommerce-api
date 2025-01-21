# NestJS E-Commerce API

## Description
A backend API for an E-Commerce system built with **NestJS** and **TypeScript**, featuring **PostgreSQL**, **JWT authentication**, **Stripe payment integration**, and **WebSockets** for real-time notifications. The API includes product management, order processing, user authentication, and Swagger documentation.

## Features
- **User Authentication & Authorization:**
  - JWT-based authentication
  - OAuth2 (Google, Facebook login)
  - Role-based access control (RBAC)
- **Product Management:**
  - CRUD operations for products
  - Image uploads (AWS S3/Cloudinary)
  - Product search, filtering, and pagination
- **Order Management:**
  - Shopping cart functionality
  - Order placement and tracking
  - Stripe/PayPal payment integration
- **Real-time Notifications:**
  - WebSockets for order updates
  - Email notifications (Nodemailer)
- **API Documentation:**
  - Swagger for API documentation
- **Testing & Deployment:**
  - Unit and E2E testing with Jest
  - CI/CD pipeline with Docker and GitHub Actions

## Installation

### Prerequisites
Ensure you have the following installed:
- Node.js (>= 16.x)
- PostgreSQL or MySQL
- Docker (optional)

### Steps to Install

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/nestjs-ecommerce-api.git
   cd nestjs-ecommerce-api
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Setup environment variables:**
   Create a `.env` file in the root directory and add the following:
   ```env
   PORT=3000
   DATABASE_URL=postgres://user:password@localhost:5432/ecommerce
   JWT_SECRET=your_secret_key
   STRIPE_SECRET=your_stripe_secret_key
   ```

4. **Run database migrations:**
   ```bash
   npm run typeorm migration:run
   ```

5. **Start the application:**
   ```bash
   npm run start:dev
   ```

6. **Access the API:**
   - Swagger UI: `http://localhost:3000/api`
   - Application runs on: `http://localhost:3000`

## Running the Tests

- **Unit Tests:**
  ```bash
  npm run test
  ```

- **E2E Tests:**
  ```bash
  npm run test:e2e
  ```

## Deployment

1. **Build the application:**
   ```bash
   npm run build
   ```

2. **Run with Docker:**
   ```bash
   docker-compose up --build
   ```

## API Endpoints

| Method | Endpoint        | Description                |
|--------|----------------|----------------------------|
| POST   | /auth/register  | Register a new user        |
| POST   | /auth/login     | Authenticate a user        |
| GET    | /products       | Get all products           |
| POST   | /orders         | Create a new order         |
| GET    | /orders/:id     | Get order details          |

## Folder Structure

```
nestjs-ecommerce-api/
├── src/
│   ├── modules/
│   │   ├── auth/
│   │   ├── products/
│   │   ├── orders/
│   ├── common/
│   ├── config/
│   ├── main.ts
│   ├── app.module.ts
├── test/
├── .env
├── package.json
├── tsconfig.json
├── README.md
```

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`feature/your-feature`).
3. Commit your changes.
4. Push to your forked repo and submit a pull request.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact
For any inquiries, please contact [tanta2358@gmail.com](mailto:tanta2358@gmail.com).

