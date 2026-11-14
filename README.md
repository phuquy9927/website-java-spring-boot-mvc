# BaloShop

A Spring Boot MVC e-commerce application for selling backpacks and lifestyle accessories. The project includes a customer storefront, shopping cart, order management, VNPay integration, admin product management, and secure authentication.

## Features

- Product catalog with pagination and product details
- User registration and login
- Role-based access control with Spring Security
- Shopping cart and order history
- VNPay payment integration
- Admin CRUD for products
- Google OAuth2 login support
- Image upload via Cloudinary
- MySQL persistence with Spring Data JPA
- JSP/JSTL views

## Tech Stack

- Java 17
- Spring Boot 3.2.2
- Spring MVC
- Spring Security
- Spring Data JPA
- MySQL
- Maven
- JSP / JSTL
- Cloudinary

## Project Structure

```text
src/
├── main/
│   ├── java/vn/qui/baloshop/
│   │   ├── config/
│   │   ├── controller/
│   │   ├── domain/
│   │   ├── repository/
│   │   ├── service/
│   │   └── baloshopApplication.java
│   └── resources/
│       └── application.properties
└── test/
    └── java/vn/qui/baloshop/
```

## Prerequisites

Before running the project, make sure you have:

- Java 17+
- Maven 3.9+
- MySQL 8+
- Optional: Google OAuth2 credentials

## Configuration

Update the database connection settings in `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/baloshop
spring.datasource.username=root
spring.datasource.password=123456
```

Create the database if it does not already exist:

```sql
CREATE DATABASE baloshop;
```

Optional Google login configuration:

```bash
export GOOGLE_CLIENT_ID=your-google-client-id
export GOOGLE_CLIENT_SECRET=your-google-client-secret
```

## Running the Application

Clone the repository and run:

```bash
./mvnw clean install
./mvnw spring-boot:run
```

On Windows, use:

```powershell
mvnw.cmd clean install
mvnw.cmd spring-boot:run
```

Then open:

```text
http://localhost:8080
```

## Default Access Points

- Home: `/`
- Login: `/login`
- Register: `/register`
- Admin products: `/admin/product`
- Order history: `/order-history`

## Notes

- The project stores session data in JDBC mode and initializes Spring Session tables automatically.
- File uploads are configured for up to 50 MB per request.
- VNPay credentials are defined in `application.properties` and may need adjustment for your environment.

## License

This project is licensed under the terms included in the repository. See `LICENSE.MD` and `LICENSE_VI.MD` for details.
