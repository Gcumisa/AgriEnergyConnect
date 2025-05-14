# Agri-Energy Connect 🌱⚡

A secure web platform connecting farmers with energy providers to track and manage agricultural products.

<img width="1440" alt="Screenshot 2025-05-14 at 23 54 36" src="https://github.com/user-attachments/assets/b1672058-3719-46b4-8f8d-f80e8e9b5dfa" />
<img width="1440" alt="Screenshot 2025-05-14 at 23 54 29" src="https://github.com/user-attachments/assets/b3a134a9-f8bc-454f-ab34-319c18c0abe6" />


## Table of Contents
- [Key Features](#key-features)
- [System Requirements](#system-requirements)
- [Setup Guide](#setup-guide)
- [Database Configuration](#database-configuration)
- [User Roles](#user-roles)
- [Troubleshooting](#troubleshooting)
- [Development Roadmap](#development-roadmap)

## Key Features

### Authentication System
- Role-based access control (Farmer/Employee)
- Secure password hashing with BCrypt
- Session management

### Farmer Functionality
- Add new products to profile
- View personal product inventory
- Update product information

### Employee Functionality
- View all farmers' products
- Filter products by:
  - Date range (production date)
  - Product category
  - Farmer profile

### Database Features
- Pre-populated demonstration data
- SQL Server backend
- EF Core migrations

## System Requirements

- **Development**:
  - Visual Studio 2022
  - .NET 9.0 SDK
  - SQL Server 2019+ or SQL Express

- **Production**:
  - Windows/Linux server
  - IIS or Kestrel
  - SQL Server

## Setup Guide

### 1. Clone Repository
bash
https://github.com/Gcumisa/AgriEnergyConnect.git
cd AgriEnergyConnect

## 2. Database Setup

powershell

# Apply migrations
dotnet ef database update
3. Configure AppSettings

json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=lab7L95SR\\SQLEXPRESS;Database=AgriEnergyConnectDb;Trusted_Connection=True;TrustServerCertificate=True;"
  }
}
4. Run Application

bash
dotnet run
Database Configuration

Pre-Populated Data

The system includes demo accounts:

Role	Email	Password
Farmer	farmer1@example.com	Password123!
Employee	employee1@example.com	Password123!

Schema Overview

Database Diagram
![AgriDiagram](https://github.com/user-attachments/assets/b2758280-79b8-4964-929e-6f23d564a6e4)


User Roles

Farmer Account

Dashboard: View personal products
Add Product:
Diagram
Code
Employee Account

Filter Products:
By date range
By product type
By farmer
Troubleshooting

Issue	Solution
Login fails	Verify password hashes in Users table
Missing products	Check Products table foreign keys
Migration errors	Run dotnet ef database update --verbose
Development Roadmap

Add reporting module
Implement product barcode scanning
Mobile app integration
Development Team
Amahle Gcumisa - Lead Developer
Luthando Gcumisa - UI/UX Designer

📧 Contact: support@agrienergyconnect.example.com

