# Bus Timer

A web application for finding bus timetables and checking when your next bus will arrive.

## Features

- **Timetable Search** – Look up buses by station and filter results to show only upcoming departures based on the current time
- **Bus Details** – View individual bus information including bus number, name, driver, and full route with stop times
- **User Accounts** – Register, log in, manage your profile, and upload a profile picture
- **Complaints** – Submit a complaint about a specific bus service
- **Suggestions** – Submit general feedback or suggestions
- **Admin Panel** – Manage buses, bus routes, users, complaints, and suggestions through a dedicated admin dashboard

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | PHP |
| Database | MySQL (via PDO) |
| Frontend | HTML5, Bootstrap 4.5.2 |
| UI Components | dselect.js |

## Project Structure

```
Bus-Timer/
├── index.php            # Home / landing page
├── timetable.php        # Bus timetable search page
├── single_bus_page.php  # Individual bus details
├── login.php            # User login
├── register.php         # User registration
├── profile.php          # User profile management
├── complaint.php        # Submit a complaint
├── suggestion.php       # Submit a suggestion
├── logout.php           # Session logout
├── conn.php             # Database connection
├── admin/               # Admin panel
│   ├── index.php        # Admin dashboard
│   ├── buses.php        # Manage buses
│   ├── bus_route.php    # Manage bus routes
│   ├── users.php        # Manage users
│   ├── complain.php     # View complaints
│   └── suggestions.php  # View suggestions
├── partials/            # Shared header and navbar includes
├── styles/              # Custom CSS
├── scripts/             # JavaScript files
└── images/              # Static images
```

## Getting Started

### Prerequisites

- PHP 7.4 or higher
- MySQL 5.7 or higher
- A web server such as Apache or Nginx (e.g. [XAMPP](https://www.apachefriends.org/) for local development)

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/zaselalk/Bus-Timer.git
   ```

2. **Move the project to your web server's document root**

   For XAMPP, copy the folder to `htdocs/`:

   ```bash
   cp -r Bus-Timer /path/to/xampp/htdocs/
   ```

3. **Create the database**

   Open your MySQL client (e.g. phpMyAdmin) and create a new database named `bus_timer`, then import the schema.

4. **Configure the database connection**

   Open `conn.php` and update the credentials to match your environment:

   ```php
   $dbHost = 'localhost';
   $dbUser = 'your_db_user';
   $dbPass = 'your_db_password';
   ```

5. **Start your web server** and navigate to `http://localhost/Bus-Timer/` in your browser.

## Usage

- Visit the home page and click **Find Bus** to search for buses by station.
- Register for an account to submit complaints or suggestions.
- Admin users can access the admin panel at `admin/index.php` to manage all application data.

## License

This project is open source. See the repository for details.
