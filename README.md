#### **School Canteen Management System**

A robust, full-stack web application designed to digitize school canteen operations. This system facilitates seamless food ordering for students and comprehensive inventory and sales management for administrators.

## Features

### **Customer (Student) Features**

* **User Authentication**: Secure registration and login system for students.
* **Real-time Menu**: Browse available food items dynamically loaded from the system.
* **Digital Cart & Checkout**: Add items to a virtual tray and place orders digitally.
* **Order Tracking & Receipts**: View current order status and generate digital receipts for pickup.
* **Profile Management**: Update user information and view personal transaction history.
* **Review System**: Leave feedback and reviews on food items.
* **Automated Notifications**: Receive email and SMS alerts regarding order status.

### **Admin Features**

* **Centralized Dashboard**: View real-time statistics including total sales and order volume.
* **Inventory CRUD**: Full control to Create, Read, Update, and Delete food items and stock levels.
* **Order Management**: Monitor incoming orders and update their status (e.g., Preparing, Ready, Collected).
* **Review Moderation**: Manage and view customer feedback.
* **SMS & Email Integration**: Direct communication with users via integrated SMS helpers and PHPMailer.
* **Vendor Sales Reports**: Generate specific sales data via dedicated API endpoints.

## Installation

### **1. Database Setup**

* Create a MySQL database (e.g., `canteen_db`).
* Import your SQL schema file into the database.
* Configure the database credentials in `db_connect.php` to match your local environment.

### **2. Directory Configuration**

* Ensure the `assets/` folder contains your CSS, JS, and image files.
* Verify that the `PHPMailer/` directory is present to enable email services.
* Create an `uploads/` folder (if not present) to store product images and set write permissions.

### **3. SMS/Mail Setup**

* Configure your SMTP settings in `services/mail_helper.php`.
* Update your API keys in `services/sms_helper.php` for SMS functionality.

---

## File Structure

```text
Finals_SCHOOLCANTEEN/
├── admin/                  # Admin-only modules and dashboard
├── api/                    # API endpoints for data retrieval
├── assets/                 # CSS, JavaScript, and static images
├── PHPMailer/              # Email handling library
├── services/               # Helper functions (SMS, Mail, Product Logic)
├── user/                   
│   └── modules/            # User-specific logic (Orders, Profile, Pages)
│       ├── auth/           # Authentication checks
│       ├── orders/         # Ordering system and receipts
│       ├── pages/          # Main user views (Home)
│       └── partials/       # Reusable UI components (Navbar, Sidebar, Modals)
├── db_connect.php          # Database connection configuration
├── index.php               # Main landing page
├── login.php               # User login entry
├── signup.php              # User registration
└── menu.json               # Static menu configuration/backup

```

---

## Technologies Used

* **PHP**: Server-side logic and session management.
* **MySQL**: Relational database for storing users, orders, and inventory.
* **Bootstrap**: Responsive UI components and layout.
* **PHPMailer**: Professional email sending integration.
* **JSON**: Data handling for menu structures.
* **AI Integration**: (`ai.php`) Potential for smart suggestions or automated queries.

## Usage

1. **Student Access**: Visit `index.php` to browse the menu; login to place an order.
2. **Admin Access**: Navigate to `/admin/login.php` to manage the canteen's stock and monitor daily sales.
3. **Order Flow**: User places order → Admin receives notification → Admin updates status → User receives SMS/Email notification.
