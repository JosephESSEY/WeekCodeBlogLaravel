# Blog Personal API - Laravel

Welcome to the **Blog Personal** project developed with Laravel. This API provides a modern and scalable blogging platform with full CRUD capabilities for articles, users, categories, and comments.

## Project Goals

* Allow users to create, read, update, and delete blog articles
* Manage users, roles, and permissions
* Organize articles by category
* Enable visitors to comment on articles
* Provide a clean, secure, and well-documented API

## Main Features

* User authentication and authorization with Laravel Sanctum or Passport
* CRUD operations for **Articles**
* CRUD operations for **Users**
* CRUD operations for **Comments**
* CRUD operations for **Categories**
* Eloquent ORM for database interactions
* Input validation with Laravel form requests
* Centralized error handling
* API resource responses
* Pagination and filtering
* Basic security (CORS, throttling, etc.)

## Database Tables

The API uses the following relational database tables:

* **users**

  * id
  * name
  * email
  * password (hashed)
  * role
  * created\_at

* **articles**

  * id
  * title
  * content
  * image
  * created\_at
  * updated\_at
  * category\_id (foreign key)
  * user\_id (foreign key, author)

* **categories**

  * id
  * name
  * description

* **comments**

  * id
  * content
  * created\_at
  * user\_id (author)
  * article\_id (target)

## Technologies Used

* PHP
* Laravel Framework
* Eloquent ORM
* MySQL or PostgreSQL
* Sanctum or Passport for API authentication
* PHPUnit for testing

## Installation

1. Clone the repository:

```bash
git clone https://github.com/your-user/blog-personal-laravel.git
```

2. Install dependencies:

```bash
composer install
```

3. Copy the example environment file and update configuration:

```bash
cp .env.example .env
```

Edit `.env` and set your database and other environment values:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=...
DB_USERNAME=...
DB_PASSWORD=...
```

4. Generate the application key:

```bash
php artisan key:generate
```

5. Run migrations:

```bash
php artisan migrate
```

6. Start the development server:

```bash
php artisan serve
```

## Testing

Run the test suite with:

```bash
php artisan test
```

or

```bash
vendor/bin/phpunit
```

## Notes

* This Laravel backend uses **Eloquent ORM** for managing all database operations.
* Input validation, error handling, and security best practices are applied throughout.
* This project is one of three separate repositories:

  * Laravel (PHP)
  * Express.js (Node)
  * Spring Boot (Java)

---
