# Income and Expense Tracker

## Overview

This is a web application developed using **Python Django** with the **MVC architecture** to help users manage their finances. The application allows users to track their income and expenses with full CRUD (Create, Read, Update, Delete) functionality. It includes user authentication and authorization, a visually appealing dashboard with charts displaying income and expense statistics, and email capabilities.

## Features

1. **User Authentication and Authorization**
   * Implemented using Django's built-in user management library.
   * Secure login, registration, password reset, and user roles.
2. **Income and Expense Tracking**
   * Users can add, view, edit, and delete income and expense entries.
   * Category-based tracking for better organization.
3. **Dashboard with Visual Insights**
   * Interactive charts and graphs display a visual summary of income and expenses.
   * Tools for filtering data by date range, categories, and other criteria.
4. **Email Notifications**
   * Configured email integration for sending notifications, confirmations, and updates.

## Technologies Used

* **Backend:** Python Django
* **Frontend:** HTML, Bootstrap CSS, JavaScript
* **Database:** SQLite (default Django database) or configurable with PostgreSQL/MySQL
* **Chart Library:** Integrated with libraries like Chart.js for interactive visuals
* **Email:** Django email backend with configurable SMTP settings

## Installation and Setup

### Prerequisites

* Python 3.8 or later
* Pip (Python package manager)
* Virtualenv (recommended)

### Steps

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/ajjiwunmi/income-expense-tracker.git
   cd income-expense-tracker
   ```
2. **Set Up a Virtual Environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```
3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
4. **Apply Migrations:**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```
5. **Create a Superuser (Admin Account):**
   ```bash
   python manage.py createsuperuser
   ```
6. **Run the Development Server:**
   ```bash
   python manage.py runserver
   ```
7. **Access the Application:**
   Open your browser and navigate to `http://127.0.0.1:8000`.

### Email Configuration

Update the email settings in the `settings.py` file:

```python
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = 'smtp.gmail.com'  # Example for Gmail
EMAIL_PORT = 587
EMAIL_USE_TLS = True
EMAIL_HOST_USER = 'your-email@example.com'
EMAIL_HOST_PASSWORD = 'your-email-password'
```

## Usage

* Register an account or log in with an existing account.
* Add income and expense entries via the user-friendly forms.
* Navigate to the dashboard to view graphical representations of your financial data.
* Receive email notifications as configured.
