# Halcon - Order Tracking Web App

Web application for “Halcon” (construction material distributor) to manage internal order workflow and allow customers to track orders by Customer Number and Invoice Number.

## Features (Scope)
### Public (Customer)
- Track order status from main screen using:
  - Customer Number
  - Invoice Number
- Shows current status:
  - ORDERED, IN_PROCESS, IN_ROUTE, DELIVERED
- If status is **DELIVERED**, shows delivery evidence photo.

### Admin Dashboard (Employees)
- Default **Admin** user can:
  - Create new users
  - Assign roles 
- Roles/Departments:
  - Admin
  - Sales
  - Purchasing
  - Warehouse
  - Route
- Orders list with search by:
  - Invoice Number
  - Customer Number
  - Date
  - Status
- Order detail:
  - Edit order data
  - Change status 
  - **Logical delete** 
- Deleted orders screen:
  - View deleted orders
  - Restore deleted orders
- Route-only evidence upload:
  - Loaded unit photo
  - Delivery evidence photo

## Business Rules
- Customers cannot register.
- Order lifecycle must be respected:
  - ORDERED → IN_PROCESS → IN_ROUTE → DELIVERED
- Evidence upload is only allowed for users with role **Route**.
- Orders are deleted logically and can be restored.

## Tech Stack
- Backend: Laravel 
- Database: MySQL


## Database
Main entities:
- roles, users, customers, orders, order_evidences, order_status_history

## Setup (Local)
### Requirements
- PHP
- Composer
- MySQL
- Laravel

### Steps
1. Clone repository:
   git clone https://github.com/rodrigopinto56/Evi1-AWD.git
   cd Evi1-AWD