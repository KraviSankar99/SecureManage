# SecureManage

SecureManage is a full-stack web application designed to provide secure management of users, customers, and invoices. Built with Angular and Spring Boot, this project features robust authentication, role-based access control, user activity tracking, and comprehensive invoice management. Dockerized for easy deployment, the app supports both development and production environments.

## Features

### **User Management**
- **Account Creation:** Create new accounts with unique email addresses and email verification.
- **Profile Management:** Users can manage their profiles (name, email, phone, bio, etc.).
- **Password Reset:** Password reset with expiring links (valid for 24 hours).
- **Authentication:** JWT-based authentication with refresh tokens for secure login.
- **Brute-Force Attack Mitigation:** Account lock after 6 failed login attempts.
- **Two-Factor Authentication:** Phone number verification for added security.
- **Activity Tracking:** Monitor user activities like login, account updates, and more.

### **Customer Management**
- **Customer Details:** Add and manage customer details (name, address, etc.).
- **Customer Status:** Assign statuses to customers (active, inactive, etc.).
- **Invoice Association:** Customers can have associated invoices.
- **Data Export:** Export customer data to spreadsheets.
- **Search & Pagination:** Search and paginate customer records by name.

### **Invoice Management**
- **Invoice Creation:** Create and manage invoices.
- **Customer Invoices:** Link invoices to customers for easy management.
- **Print & Download:** Print invoices for mailing, and export invoices in both spreadsheet and PDF formats.

## **Tech Stack**

### **Frontend**
- **Angular 17** - Framework for building the client-side application.
- **TypeScript** - Programming language for the frontend.
- **HTML, CSS** - Structure and styling for the frontend.

### **Backend**
- **Spring Boot** - Java framework for building the backend REST API.
- **Java** - Primary programming language used for backend logic.
- **Spring Security** - Security framework for user authentication and authorization.
- **JWT (JSON Web Tokens)** - Used for secure, token-based authentication.
- **MySQL** - Relational database for storing user, customer, and invoice data.
- **Spring Data JPA** - To simplify database interaction using Java persistence.

### **Dockerization**
- **Docker** - The entire application (both frontend and backend) is dockerized for easy setup, scalability, and deployment.
- **Docker Compose** - Used to manage multi-container Docker applications, enabling seamless orchestration of the frontend, backend, and database containers.

### **Other Technologies**
- **PostgreSQL (for testing & staging environments)** - Used in some environments for database management.
- **Karma & Jasmine** - For unit and integration testing in Angular.
- **Maven** - For managing backend dependencies and building the Spring Boot application.
- **Nginx (for reverse proxy)** - Configured for production environments to serve the Angular frontend.

## **Installation and Setup**

### **Backend (Spring Boot)**

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/SecureManage.git
   cd SecureManage
   ```

2. Configure the database connection in `src/main/resources/application.properties`:
   - Update the database URL, username, and password.

3. Build and run the Spring Boot application:
   ```sh
   mvn spring-boot:run
   ```

### **Frontend (Angular)**

1. Navigate to the frontend directory:
   ```sh
   cd frontend
   ```

2. Install dependencies:
   ```sh
   npm install
   ```

3. Start the development server:
   ```sh
   ng serve
   ```

4. Open the app in your browser at `http://localhost:4200/`.

### **Dockerized Setup**

To run the full application (both frontend and backend) in Docker containers:

1. Build the Docker images:
   ```sh
   docker-compose build
   ```

2. Start the application:
   ```sh
   docker-compose up
   ```

3. Access the application:
   - Frontend will be available at `http://localhost:4200/`.
   - Backend API will be available at `http://localhost:8080/`.

### **Testing**

1. **Run unit tests** (Frontend):
   ```sh
   ng test
   ```

2. **Run end-to-end tests** (Frontend):
   ```sh
   ng e2e
   ```

3. **Run backend tests** (Spring Boot):
   ```sh
   mvn test
   ```

## **Project Size**

This project is a **medium to large-scale application** designed to manage secure user and customer information, invoicing, and more. It incorporates secure authentication, robust data handling, and seamless integration between the front-end and back-end, making it suitable for real-world enterprise environments.

