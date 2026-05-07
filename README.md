# QuickCourt Backend

A robust RESTful API backend for the QuickCourt application, built with **Laravel 10**. This backend powers the sports venue booking system, food and beverage (F&B) ordering, and secure payment processing.

## 🚀 Key Features

- **Authentication:** Secure login and registration powered by **Firebase** and **Laravel Sanctum**.
- **Role-Based Access:** Dedicated features and dashboards for **Users**, **Venue Owners**, and **Admins**.
- **Venue Management:** Comprehensive endpoints to manage venues, facilities, available time slots, and promotions.
- **Booking System:** Seamless sports venue booking flow, including status tracking and history.
- **Food & Beverage (F&B):** Integrated cart and ordering system for venue-specific F&B menus.
- **Payment Gateway:** Integrated with **Midtrans** for secure payment processing and manual receipt uploads.

## 🛠️ Technology Stack

- **Framework:** Laravel 10 (PHP 8.1+)
- **Authentication:** Laravel Sanctum & Firebase PHP (`kreait/firebase-php`)
- **Payments:** Midtrans PHP (`midtrans/midtrans-php`)
- **HTTP Client:** GuzzleHTTP

## 📦 Requirements

- PHP >= 8.1
- Composer
- MySQL / PostgreSQL (or any supported database)
- Firebase Project Credentials
- Midtrans Server Key

## ⚙️ Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Fathinda/Backend_QuickCourt.git
   cd Backend_QuickCourt
   ```

2. **Install dependencies:**
   ```bash
   composer install
   ```

3. **Set up the environment:**
   Copy the example environment file and generate an application key.
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

4. **Configure your `.env` file:**
   Update your database credentials, Firebase configuration, and Midtrans keys in the `.env` file.

5. **Run Database Migrations:**
   ```bash
   php artisan migrate
   ```
   *(Add `--seed` if you have database seeders ready).*

6. **Start the local development server:**
   ```bash
   php artisan serve
   ```
   The API will be accessible at `http://localhost:8000/api`.

## 📂 Project Structure Highlights

- **`routes/api.php`**: Contains all the API endpoints grouped by functionality and middleware (Sanctum auth, roles).
- **`app/Http/Controllers/API`**: Houses the logic for handling incoming requests (Booking, F&B, Venues, Users, Owner Dashboards).
- **`app/Models`**: Eloquent models representing database tables like `User`, `Venues`, `Booking`, `Fnb_order`, `Payment`, etc.

---
*Built for the QuickCourt App ecosystem.*
