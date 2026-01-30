# Authentication & Account Management System (Login • Dashboard • Account Settings)  

<p align="center">
  <a href="https://www.jminnovatechsolution.co.ke" target="_blank">
    <img src="https://www.jminnovatechsolution.co.ke/assets/img/iconbg-512.png" width="300" alt="JM Innovatech Logo">
  </a>
</p>

---

## Overview

This **Laravel-based Authentication System** built for any application that requires secure user login, registration, password recovery, dashboard access, and account management.

It provides a complete, production-ready authentication flow including email/password login, Google-based accounts, OTP password resets, profile management, and session security — suitable for any modern web system that can be integrated into:
- Web applications
- SaaS platforms
- Admin dashboards
- Enterprise systems
- Subscription-based services

The system focuses strictly on user authentication, dashboard access, and account settings, making it reusable across different projects.
---

## Key Features

### 1. Login System
- Secure login using email and password
- Server-side credential validation
- Session regeneration on successful login
- “Remember Me” support
- Automatic redirection for already authenticated users
- Account suspension checks (blocked users cannot log in)

### 2. User Registration
- New user account creation
- Unique email enforcement
- Password confirmation and minimum strength validation
- Automatic login after successful registration
- Unique username generation

### 3. Logout
- Secure logout with session invalidation
- Protection against unauthorized logout attempts

## Password Recovery & Reset

### 1. Forgot Password (OTP-Based)
- Email-based password reset using One-Time Password (OTP)
- Secure OTP generation (5-digit code)
- OTP expiration handling (time-limited validity)
- OTP stored and managed per user
- Email delivery of OTP using Laravel Mail

### 2. OTP Resend
- Resend OTP functionality
- OTP regeneration on resend
- Resend attempt tracking
- Reset expiration window on resend

### 3. Password Reset Flow
- OTP verification before allowing password reset
- Invalid and expired OTP handling
- Secure password update after OTP verification
- Automatic cleanup of used OTP records

## Account & Profile Management

### 1. Account Settings
- Authenticated users can:
- Update name and email address
- Upload and update profile image
- Change password securely
- Update password even for Google-registered accounts
- Automatic unlinking of Google account when email is changed

### 2. Password Update Security
- Current password verification for non-Google users
- Password hashing using Laravel’s Hash system
- Strong password validation rules
- Protection against incorrect current password attempts

## Social Authentication Support

### 1.Google-Registered Accounts
- Supports users registered via Google OAuth
- Allows conversion from Google login to password-based login
- Automatically disables Google-only restriction when password is set

#### 🔑 Google OAuth Setup Guide
To enable the Google Sign-in feature, follow these steps to configure your environment:

**1. Obtain Credentials from Google Cloud Console**
* Go to the [Google Cloud Console](https://console.cloud.google.com/).
* **Create a New Project** and navigate to **APIs & Services > Credentials**.
* Click **Create Credentials > OAuth client ID**.
* Select **Web application** as the application type.
* **Authorized redirect URIs:** Add `https://your url/auth/google/callback` (or your production URL).


**2. Update Environment Variables (`.env`)**
Copy the Client ID and Secret into your project's `.env` file:

## Installation & Setup

### 1. **Clone the repository**
```bash
git clone git@github.com:Jmuthoga/Authentication-Account-Management-System.git
cd Authentication-Account-Management-System
```
### 2. **Install dependencies**
   ```bash
   composer install
   npm install
   npm run dev
   ```
### 3. **Configure .env**
  ```bash
    # App Configuration
    APP_NAME=Authentication
    APP_ENV=local
    APP_KEY=base64:YOUR_APP_KEY
    APP_DEBUG=true
    APP_URL=http://localhost:8000
    WEBSITE_NAME="Authentication & Account Management System"
    
    # Database
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=your_database
    DB_USERNAME=your_username
    DB_PASSWORD=your_password
    
    # Mail for notifications
    MAIL_MAILER=smtp
    MAIL_HOST=your_mail_host
    MAIL_PORT=your_mail_port
    MAIL_USERNAME=your_username
    MAIL_PASSWORD=your_password
    MAIL_ENCRYPTION=tls
    MAIL_FROM_ADDRESS="info@example.com"
    MAIL_FROM_NAME="${APP_NAME}"

    # Google OAuth Credentials
    GOOGLE_CLIENT_ID=your-client-id.apps.googleusercontent.com
    GOOGLE_CLIENT_SECRET=your-client-secret
    GOOGLE_REDIRECT_URL="${APP_URL}/auth/google/callback"
```
### 4. **Run Migrations & Seeders**
 ```bash
   php artisan migrate --seed
```
### 5. **Serve the Application**
```bash
    php artisan serve
```

## Contributing
- Fork the repository, make your changes, and submit a pull request
- Follow PSR coding standards and keep commits clean

## Contact

<p>
  <a href="https://wa.me/254791446968" target="_blank">
    <img src="https://img.icons8.com/color/48/000000/whatsapp--v1.png" width="24" alt="WhatsApp"/> 
    Chat with us on WhatsApp
  </a>
</p>



## License

This project is licensed under the **MIT License**.  
See the [LICENSE](LICENSE) file for details.



