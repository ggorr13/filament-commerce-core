# 🛒 Filament Commerce Core

[](https://laravel.com)
[](https://filamentphp.com)
[](https://php.net)
[](https://opensource.org/licenses/MIT)

A high-performance, modular E-commerce Administration Engine built with **Laravel 13** and **Filament PHP v4**. This core focuses on clean architecture, granular security, and scalable business logic.

## 🏗 Architecture Principles

The project follows a **Senior-level architecture** to ensure maintainability:

* **Clean Separation:** Resources are decoupled into `Schemas` (Forms), `Tables` (Data Grids), and `Pages` (Logic).
* **RBAC (Role-Based Access Control):** Fully integrated with **Filament Shield** for precise permission management.
* **Security First:** Automated password hashing, session security, and sensitive data protection via Filament dehydration.
* **Scalability:** Ready for large-scale product catalogs and complex user hierarchies.

## 📂 Project Structure

```text
app/Filament/Resources/
└── Users/
    ├── Pages/          # View, List, Edit, Create logic
    ├── Schemas/        # Business rules for Forms & Infolists
    ├── Tables/         # Data table columns, filters, and actions
    └── UserResource.php # Resource configuration & navigation
```

## 🚀 Key Features Implemented

* **Advanced User Management:** Full CRUD with dedicated Schema/Table classes.
* **Role & Permission UI:** Manage Spatie roles and permissions directly from the dashboard.
* **Badge-based Roles:** Visual role identification in user tables.
* **Global Search:** Command-palette search for users by name and email.
* **Admin Shield:** Protection of all administrative routes and actions.

## 🛠 Installation & Setup

```bash
# 1. Clone & Enter
git clone https://github.com/ggorr13/filament-commerce-core.git
cd filament-commerce-core

# 2. Dependencies
composer install
npm install && npm run build

# 3. Environment
cp .env.example .env
php artisan key:generate

# 4. Database & Auth Setup
php artisan migrate
php artisan shield:install
php artisan shield:generate --all

# 5. Create Super Admin
php artisan make:filament-user
php artisan shield:super-admin --user=1
```

## 🛡 Security Note

This repository is maintained using **Personal Access Tokens (PAT)**. Never share or commit your GitHub tokens or `.env` files. Ensure `APP_DEBUG` is set to `false` in production environments.

-----

## 👨‍💻 Author

**Gor** Senior Software Engineer | Backend Specialist  
[GitHub Profile](https://www.google.com/search?q=https://github.com/ggorr13)

-----

*© 2026 Filament Commerce Core. Optimized for performance and clean code.*
