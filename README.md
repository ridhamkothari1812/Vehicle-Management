# Vehicle Parking

A multi-user web application designed to manage vehicle parking lots, parking spaces, reservations, and parking records efficiently.

## 📌 Project Overview

**Vehicle Parking** is a web-based parking management system that allows administrators to manage parking lots and parking spaces, while users can reserve available parking spots, manage their parking sessions, and view their parking history.

The system is designed for **four-wheeler vehicle parking** and provides separate functionalities for administrators and registered users.

The application automates parking spot allocation, reservation management, parking duration calculation, and parking cost calculation.

---

## 🎯 Project Objectives

* Manage multiple parking lots from a centralized system.
* Automatically generate parking spots according to parking lot capacity.
* Provide secure user registration and authentication.
* Provide separate dashboards for administrators and users.
* Allow users to reserve available parking spots.
* Track parking entry and exit timestamps.
* Automatically calculate parking duration and parking charges.
* Maintain complete parking and reservation history.
* Provide graphical summaries and statistics for parking management.

---

## 👥 User Roles

### Admin

The administrator can:

* Create, update, and delete parking lots.
* Manage parking lot capacity and parking spots.
* View the current status of parking spots.
* View parking and reservation records.
* View registered users and their parking records.
* Monitor parking lot statistics.
* View graphical summaries of parking activity and revenue.

### User

Registered users can:

* Create an account and log in securely.
* View available parking lots.
* Reserve an available parking spot.
* Occupy and release a parking spot.
* View active parking sessions.
* View complete parking history.
* Track reservation and parking timestamps.
* View parking duration.
* View automatically calculated parking costs.
* Update their profile information.

---

## ⚙️ Key Features

### Authentication & Authorization

* User registration and login.
* Predefined administrator account.
* Role-based access control.
* Protected routes and sessions.
* Password hashing for secure password storage.
* Unauthorized users are restricted from accessing protected pages.

### Parking Lot Management

* Create new parking lots.
* Edit existing parking lot information.
* Delete parking lots.
* Automatically generate parking spots based on maximum capacity.
* View parking spot availability and status.

### Parking Reservation

* View available parking lots.
* Automatically allocate the first available parking spot.
* Reserve parking spots without manual spot selection.
* Maintain reservation history.

### Parking Management

* Occupy reserved parking spots.
* Release parking spots after use.
* Record entry and exit timestamps.
* Automatically calculate parking duration.
* Automatically calculate the total parking cost.

### History & Reports

* User-specific parking history.
* Active parking records.
* Administrative parking records.
* Parking lot statistics.
* Revenue and occupancy summaries.
* Graphical representation of parking data.

### Form Validation & Security

* Frontend form validation using HTML5 and JavaScript.
* Backend validation using Python.
* Regular-expression based validation for required fields.
* Password visibility toggle.
* Secure password hashing.

---

## 🛠️ Technology Stack

| Technology      | Purpose                                  |
| --------------- | ---------------------------------------- |
| **Python**      | Backend development                      |
| **Flask**       | Web application framework                |
| **Flask-Login** | Authentication and session management    |
| **SQLAlchemy**  | Database ORM                             |
| **SQLite**      | Database                                 |
| **HTML5**       | Frontend structure                       |
| **CSS3**        | Styling                                  |
| **JavaScript**  | Client-side functionality and validation |
| **Chart.js**    | Data visualization                       |
| **Jinja2**      | Dynamic HTML templating                  |

---

## 🗂️ Core Modules

The application is divided into the following major modules:

1. **Authentication Module**

   * Registration
   * Login
   * Logout
   * Password management
   * Role-based access

2. **Admin Module**

   * Dashboard
   * Parking lot management
   * Parking spot management
   * User management
   * Parking records
   * Statistics and summaries

3. **User Module**

   * User dashboard
   * Parking lot browsing
   * Reservation
   * Active parking
   * Parking history
   * Profile management

4. **Parking Management Module**

   * Spot allocation
   * Reservation tracking
   * Occupancy management
   * Spot release
   * Duration calculation
   * Cost calculation

5. **Analytics Module**

   * Parking statistics
   * Parking lot summaries
   * Revenue visualization
   * Occupancy visualization

---

## 🗄️ Database Design

The application uses a relational database to maintain parking and user information.

The major entities include:

* **User**
* **Admin**
* **Parking Lot**
* **Parking Spot**
* **Reserve Parking Spot**

### Relationships

* A user can have multiple parking/reservation records.
* A parking lot can contain multiple parking spots.
* A parking spot can have multiple reservation records over time.
* Parking records maintain information about reservation, occupancy, release time, duration, and cost.

The database tables are created programmatically through the application rather than being manually created.

---

## 🚀 Installation & Setup

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd vehicle-parking
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

### 3. Activate the virtual environment

**Windows:**

```bash
venv\Scripts\activate
```

**Linux / macOS:**

```bash
source venv/bin/activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Run the application

```bash
python app.py
```

The application will start on the local Flask development server.

Open the URL shown in the terminal in your web browser.

---

## 🔐 Authentication

The application supports two types of access:

**Administrator**

* Uses the predefined administrator credentials.
* Has access to administrative features and parking management.

**User**

* Creates an account through registration.
* Logs in using registered credentials.
* Has access to user-specific parking functionality.

> Update the administrator credentials according to the configuration present in the project before deployment.

---

## 📊 Dashboard & Visualization

The application provides dashboards for both administrators and users.

The administrative dashboard provides an overview of parking activity through:

* Parking lot statistics
* Occupancy information
* Revenue-related information
* Graphical charts
* Parking records

Charts and visualizations are implemented using **Chart.js**.

---

## 🔄 Parking Workflow

The basic parking workflow is:

```text
User Registration
       ↓
User Login
       ↓
View Available Parking Lots
       ↓
Reserve Available Parking Spot
       ↓
Occupy Parking Spot
       ↓
Vehicle Parking Session
       ↓
Release Parking Spot
       ↓
Calculate Parking Duration
       ↓
Calculate Parking Cost
       ↓
Store Parking History
```

---

## 🧪 Validation & Error Handling

The application includes validation at both frontend and backend levels.

* Required-field validation.
* Input format validation.
* User registration validation.
* Password validation.
* Backend input validation.
* Handling of empty parking records.
* Handling of occupied parking spots.
* Validation of parking-related calculations.

Additional error handling has been implemented to prevent dashboard and parking-detail pages from failing when certain parking records are unavailable or currently active.

---

## 🔮 Future Enhancements

The application can be further enhanced with:

* Online payment integration.
* QR-based parking entry and exit.
* Vehicle number plate recognition.
* Real-time parking availability.
* Email/SMS notifications.
* Multiple vehicle types and pricing plans.
* Advanced analytics and reporting.
* Cloud database integration.
* REST API integration.
* Mobile application support.
* Deployment on a cloud platform.

---

## 📁 Project Structure

The project follows a Flask-based application structure consisting of:

```text
vehicle-parking/
│
├── app.py
├── requirements.txt
├── README.md
│
├── templates/
│   ├── admin/
│   ├── user/
│   └── ...
│
├── static/
│   ├── css/
│   ├── js/
│   └── ...
│
├── database/
│   └── ...
│
└── other project files
```

*The exact structure may vary depending on the current implementation of the project.*

---

## 📌 Project Status

**Project Status: Completed**

The core parking management functionality, authentication, reservation system, parking history, cost calculation, validation, dashboards, and data visualization have been implemented.

---

## 👨‍💻 Project Information

**Project Title:** Vehicle Parking
**Project Type:** Web Application
**Domain:** Parking Management System
**Backend:** Python / Flask
**Database:** SQLite
**Frontend:** HTML, CSS & JavaScript

---

## 📄 License

This project is intended for academic and educational purposes.
