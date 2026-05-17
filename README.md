# ✈️ Omnira Airlines — Airline Reservation and Ticketing System

> A web-based airline reservation and ticketing platform developed as a course requirement for **CSC181** at the **College of Computer Studies, Mindanao State University**.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [System Architecture](#system-architecture)
- [User Roles](#user-roles)
- [Use Cases](#use-cases)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Team](#team)
- [References](#references)

---

## Overview

The **Omnira Airline Reservation and Ticketing System** is a centralized, secure, and user-friendly digital platform designed to streamline the full airline booking lifecycle — from flight search to e-ticket issuance. It eliminates the inefficiencies of manual reservation processes by automating booking, payment, and ticket generation workflows for both passengers and airline staff.

---

## Features

### Passenger-Facing
- 🔍 **Flight Search & Availability** — Search flights by destination, origin, date, and airline; view real-time seat availability and pricing.
- 📋 **Booking System (PNR Creation)** — Select a flight, choose a seat, enter passenger details, and receive an auto-generated Passenger Name Record (PNR).
- 💳 **Payment Processing** — Secure payment via card or e-wallet, integrated with a third-party payment gateway, with receipt generation upon success.
- 🎟️ **E-Ticket Issuance** — Automatic generation and email delivery of a downloadable/printable electronic ticket after confirmed payment.
- 🔎 **Booking Retrieval** — Look up existing bookings anytime using PNR and last name; resend confirmation email or e-ticket.
- 🏷️ **Promo Code Support** — Apply discount codes during the booking process.

### Admin / Staff Portal
- ✈️ **Flight Schedule Management** — Add, edit, or remove flight schedules with validation.
- 👥 **Booking & User Management** — View and manage all passenger bookings and user data.
- 📊 **Reports & Analytics** — Access booking manifests and sales summary reports.
- 🔐 **Secure Access Control** — Role-based permissions separating Admin and Passenger access.

### Security
- 🔒 Encrypted user credentials and payment data
- 🛡️ Role-based access control (RBAC)
- 🔑 Secure authentication mechanisms

---

## System Architecture

The system is built around six core functional modules:

**1. Flight Search & Availability**
Allows passengers to search for flights by destination, origin, date, and airline, and view real-time seat availability and pricing.

**2. Booking System / PNR Creation**
Handles flight selection, seat choosing, passenger information collection, and auto-generation of a unique Passenger Name Record (PNR).

**3. Payment Processing**
Facilitates secure payments via card or e-wallet through an integrated third-party payment gateway, and generates validated receipts upon success.

**4. E-Ticket Issuance**
Automatically generates and delivers an electronic ticket to the passenger's email upon payment confirmation, with an option to print or download.

**5. Admin / Staff Management**
Provides a secure portal for airline staff to manage flight schedules, oversee bookings, handle user data, and generate operational reports.

**6. Security & Data Protection**
Enforces data encryption, role-based access control (RBAC), and secure authentication to protect user credentials and financial information.
​```

### Key Data Entities
| Entity   | Description |
|----------|-------------|
| `Users`  | Account info for Passengers and Admins (credentials, roles) |
| `Flights` | Schedule details — origin, destination, times, price, seat inventory |
| `Bookings` | PNR records linking a Flight to a Passenger |
| `Payments` | Transaction records with status (pending, completed, failed) |

---

## User Roles

| Role | Capabilities |
|------|-------------|
| **Passenger** | Search flights, book tickets, process payments, retrieve bookings, download e-tickets |
| **Admin / Staff** | All Passenger capabilities + manage flights, view all bookings, manage users, access reports |
| **System** | Automated PNR generation, notifications, security enforcement, gateway communication |

---

## Use Cases

| ID | Use Case | Actor |
|----|----------|-------|
| UC-001 | Search Destination | Passenger |
| UC-002 | Book Flight | Passenger |
| UC-003 | Payment for Booking | Passenger |
| UC-004 | Generate E-Ticket | Passenger |
| UC-005 | Manage Flight Schedules | Admin |

---

## Tech Stack

> ⚙️ *Technology choices are guided by the project's constraints — open-source preferred, web-based, and browser-compatible.*

| Layer | Technology |
|-------|-----------|
| Frontend | *(e.g., HTML/CSS/JavaScript or React)* |
| Backend | *(e.g., Node.js / PHP / Django)* |
| Database | *(e.g., MySQL / PostgreSQL)* |
| Payment Gateway | *(e.g., PayMongo / Stripe)* |
| Version Control | Git / GitHub |
| Communication | Google Meet |
| Cloud Storage | Google Drive / OneDrive |

> Update this section with the actual technologies used during implementation.

---

## Getting Started

### Prerequisites
- Node.js / PHP / Python *(depending on stack used)*
- A supported relational database (MySQL or PostgreSQL)
- Git

### Installation

​```bash
# Clone the repository
git clone https://github.com/<your-org>/omnira-airlines.git
cd omnira-airlines

# Install dependencies
npm install   # or: composer install / pip install -r requirements.txt

# Configure environment variables
cp .env.example .env
# Fill in DB credentials, payment gateway keys, mail settings

# Run database migrations
npm run migrate   # or equivalent

# Start the development server
npm run dev
​```

## Project Structure

The repository is organized as follows:

- **src/frontend/** — UI components and pages
- **src/backend/** — Server-side logic and APIs
- **src/database/** — Migrations and seed data
- **src/config/** — App and environment configuration
- **docs/** — SRS, SDD, and other documentation
- **tests/** — Unit and integration tests
- **.env.example** — Environment variable template
- **README.md** — Project documentation

---

## Environment Variables

Before running the project, copy `.env.example` to `.env` and fill in the following values:

**Database**
- `DB_HOST` — Hostname of your database server (e.g., `localhost`)
- `DB_NAME` — Name of the database (e.g., `omnira_db`)
- `DB_USER` — Database username
- `DB_PASS` — Database password

**Payment Gateway**
- `PAYMENT_GATEWAY_KEY` — API key from your payment provider (e.g., PayMongo or Stripe)

**Mail / Notifications**
- `MAIL_HOST` — SMTP server host (e.g., `smtp.example.com`)
- `MAIL_PORT` — SMTP port (e.g., `587`)
- `MAIL_USER` — Email address used for sending notifications
- `MAIL_PASS` — Password for the mail account

---

## Team

| Name | Role |
|------|------|
| **Mohammad Zulkifli S. Macadato** | Team Lead |
| **Amber Miguel B. Malinis** | Documentation Lead |
| **Junnel Francis S. Jonson** | Frontend Developer |
| **Mohammad Hosni U. Palantig** | Backend Developer |
| **Aliyah M. Salmorin** | QA Tester / UI-UX Designer |

---

## References

- IEEE Std 29148-2018 — Requirements Engineering
- IEEE Std 830-1998 — Software Requirements Specifications
- ISO/IEC 27001 — Information Security Management Systems
- Sommerville, I. (2015). *Software Engineering* (10th ed.). Pearson.
- Pressman, R. S. (2019). *Software Engineering: A Practitioner's Approach*. McGraw-Hill.
- [GeeksforGeeks — Airline Reservation System](https://www.geeksforgeeks.org/airline-reservation-system/)
- IATA Airline Industry Data Protection Guidelines

---

> *Developed as a partial fulfillment of the requirements for CSC181 — College of Computer Studies, Mindanao State University. November 2025.*
