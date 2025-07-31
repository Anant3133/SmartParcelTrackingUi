# Smart Parcel Tracking System

A full-stack web application for parcel tracking in a logistics system using QR codes.  
It supports three user roles: *Sender, **Handler, and **Admin* to create, update, and monitor parcels securely and efficiently.

---

## Table of Contents

- [Project Overview](#project-overview)  
- [Features](#features)  
- [Tech Stack](#tech-stack)  
- [Database](#database)  
- [Frontend Dependencies](#frontend-dependencies)  
- [Backend Dependencies](#backend-dependencies)  
- [Setup Instructions](#setup-instructions)  
- [Screenshots](#screenshots)  

---

## Project Overview

- Parcel tracking system with QR code integration.  
- Three user roles:  
  - *Sender*: Creates parcels and generates QR codes.  
  - *Handler*: Scans QR codes and updates parcel status.  
  - *Admin*: Manages users, parcels, tamper alerts, and analytics.  
- Automated tamper detection to flag suspicious parcel status updates.  
- Map-based route visualization and interactive dashboards.

---

## Features

- *Parcel Lifecycle Tracking*  
  - Parcel statuses:  
    - Received  
    - Packed  
    - Shipping  
    - Out for Delivery  
    - Delivered  
  - QR code generation and scanning for parcels.  

- *Tamper Detection*  
  - Flags skipped steps or very rapid status changes (less than 1 hour).  
  - Alerts displayed prominently on Admin Dashboard.

- *Admin Dashboard*  
  - Manage users and parcels.  
  - View tamper alerts and analytics charts.  
  - Route tracking on maps (using Leaflet).  

- *User Profiles*  
  - Role-based dashboards.  
  - Editable avatar, banner, and personal info.  
  - Password reset and change functionalities.

- *Security*  
  - JWT-based authentication.  
  - Protected API routes.

---

## Tech Stack

- *Frontend*:  
  - React.js  
  - Tailwind CSS  
  - Leaflet (maps)  
  - Chart.js (data visualization)  
  - HTML5 QR code scanner  

- *Backend*:  
  - .NET Core (C#)  
  - Entity Framework Core  
  - MySQL  
  - JWT Authentication  

- *Testing Tools*:  
  - Postman  
  - JMeter  
  - Jira  
  - Zephyr  

---

## Database

- *Database Used*: MySQL  
- *Schema Includes*:  
  - Tables for users, parcels, parcel status history, tamper alerts, and roles.  
  - Relationships:  
    - Users linked to parcels (Sender and Handler).  
    - Parcel status changes logged with timestamps.  
    - Tamper alerts linked to parcels with detailed info.  
- *Setup Notes*:  
  - Import provided SQL schema or run migrations (if applicable).  
  - Update connection string in backend appsettings.json.  

---

## Frontend Dependencies

Use npm install <package> to add these packages inside the frontend folder.

- *Core Libraries*  
  - react, react-dom: React framework core  
  - react-router-dom: Routing and navigation  

- *Styling*  
  - tailwindcss, postcss, autoprefixer: Styling and CSS processing  
  - flowbite: UI components library  
  - @heroicons/react, lucide-react, react-icons: Icons  

- *HTTP & State*  
  - axios: HTTP client for API requests  

- *QR & Maps*  
  - html5-qrcode: QR code scanning in browser  
  - leaflet, react-leaflet: Map rendering and interactivity  

- *Data Visualization*  
  - chart.js, react-chartjs-2: Charts and graphs  

- *Animations & Effects*  
  - framer-motion, gsap: Animations and transitions  

- *Notifications*  
  - react-hot-toast, react-toastify: Toast notifications  

---

## Backend Dependencies

Use .NET CLI commands to install these packages in the backend project.

- Microsoft.AspNetCore.Authentication.JwtBearer  
  Adds JWT authentication for API security.

- Microsoft.EntityFrameworkCore  
  Entity Framework Core ORM for database operations.

- Microsoft.EntityFrameworkCore.Design  
  Tools for database migrations.

- Microsoft.EntityFrameworkCore.SqlServer  
  SQL Server database provider (used alongside MySQL if needed).

- QRCoder  
  Generates QR codes server-side.

- BCrypt.Net-Next  
  Password hashing for secure user credentials.

- Swashbuckle.AspNetCore  
  Adds Swagger UI for API documentation.

---

## Setup Instructions

### Frontend

1. Go to frontend folder:  
   ```bash
   cd frontend

2. Install dependencies:

npm install


3. Run development server:

npm start




---

Backend

1. Go to backend folder:

cd backend


2. Restore packages:

dotnet restore


3. Build the project:

dotnet build


4. Run the project:

dotnet run




---

Database

Install and run MySQL server.

Import the SQL schema file provided (if available):

mysql -u username -p database_name < schema.sql

Update your database connection string in appsettings.json (backend).



---

Screenshots

Sender Dashboard — Parcel creation with QR code

<img width="1877" height="760" alt="Screenshot 2025-07-15 160424" src="https://github.com/user-attachments/assets/042e1530-3b17-4df6-8a83-f6646af4ddf1" />

Handler Dashboard — QR code scanner and status update

<img width="1906" height="860" alt="Screenshot 2025-07-10 150917" src="https://github.com/user-attachments/assets/c4951980-d962-42b7-b950-c65dc552166d" />

<img width="427" height="445" alt="Screenshot 2025-07-10 151934" src="https://github.com/user-attachments/assets/52a9c887-d4ef-4417-9559-ebdffca5d5bd" />

Admin Dashboard — Parcel list, tamper alerts, and analytics charts

<img width="765" height="352" alt="Screenshot 2025-07-31 123423" src="https://github.com/user-attachments/assets/c3e37ebd-f6ec-4530-aa55-3f84114e9810" />

<img width="763" height="363" alt="image" src="https://github.com/user-attachments/assets/0693a2c7-84d5-440d-991a-37d71e177338" />

<img width="761" height="347" alt="image" src="https://github.com/user-attachments/assets/72dc693e-49fb-4442-b394-e0ea20f6d403" />

<img width="841" height="551" alt="image" src="https://github.com/user-attachments/assets/7f7ad6a0-1980-41fd-b7bb-fb12830d3a0d" />

Map view showing parcel routes

<img width="815" height="542" alt="Screenshot 2025-07-10 151741" src="https://github.com/user-attachments/assets/ce7b62b7-40ca-42bb-b5b2-53ba22905113" />

Profile page with editable avatar and personal details

<img width="1899" height="863" alt="Screenshot 2025-07-15 155151" src="https://github.com/user-attachments/assets/63b543f7-a626-4add-92f9-b16b1d5fbb87" />


---
