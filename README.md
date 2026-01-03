# VincentMobile Database System

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sharon-Tseng/VincentMobile_Database_System)

A comprehensive interactive database management system for Vincent Mobile, an online mobile phone and tablet retail platform with integrated trade-in services.

## 📋 Overview

Vincent Mobile aims to develop a system that allows members to purchase the latest mobile phones and tablets online while facilitating offline trade-in services. This repository contains Jupyter notebooks implementing the database-backed application interfaces for different user roles.

## 🏗️ System Architecture

The system consists of **3 main modules** supporting different actors:

1. **Customers and Members** - Online shopping and trade-in services
2. **Administrators and Managers** - Product and order management, reporting
3. **Officers** - Trade-in processing and customer service

## 📓 Notebooks

### Main Notebooks

- **[Customer_and_Member_Final_OpFeature_Merged.ipynb](Customer_and_Member_Final_OpFeature_Merged.ipynb)** - Complete customer and member module with operational features
- **[Admin_officer_merged.ipynb](Admin_officer_merged.ipynb)** - Merged administrator and officer module implementation
- **[m3m4_v_ST.ipynb](m3m4_v_ST.ipynb)** - Administrator/Manager and Officer modules implementation (older version)
- **[Customer_and_Member_final.ipynb](Customer_and_Member_final.ipynb)** - Customer and member module (older version)

## 🎯 Key Features

### Administrator Functions
- Maintain product catalog (add new products, fade out obsolete items)
- Manage inventory with stock replenishment updates
- Review and process confirmed orders
- Update delivery status ("To be delivered", "Completed")
- Generate operational and managerial reports

### Officer Functions
- Record trade-in device information in the database
- Process customer trade-in decisions
- Inspect devices and provide trade-in offers
- Update order pricing based on trade-in agreements

### Customer/Member Functions
- **Account Management**: Register as a member before making purchases
- **Product Discovery**: Search products using keywords
- **Shopping Cart**: Store desired products with intelligent out-of-stock handling
- **Order Management**: Purchase multiple products in a single transaction
- **Payment Processing**: Complete orders with credit card information
- **Trade-in Service**: Submit old device information for trade-in evaluation

## 🔧 Technical Stack

- **Database**: Oracle Database (cx_Oracle)
- **Interface**: Google Colab / Jupyter Notebook
- **Libraries**: 
  - `cx_Oracle` - Oracle database connectivity
  - `pandas` - Data manipulation
  - `ipywidgets` - Interactive UI components
  - `google.colab.widgets` - TabBar for module navigation

## 🚀 Getting Started

### Prerequisites

- Access to Oracle Database (HKUST imz409 server)
- Google Colab or Jupyter Notebook environment

### Setup

1. Open any notebook in Google Colab or Jupyter
2. Run the Oracle Instant Client installation cells
3. Configure database connection with credentials:
   ```python
   HOST_NAME = "imz409.ust.hk"
   PORT_NUMBER = "1521"
   SERVICE_NAME = "imz409"
   USERNAME = "your_username"
   PASSWORD = "your_password"
   ```

### Running the Application

1. Open the desired module notebook
2. Execute cells sequentially
3. Interact with the widget-based interface

## 📦 Business Logic

### Shopping Cart Behavior
- Cart items persist across sessions until purchased
- Out-of-stock products are automatically hidden during checkout
- Items reappear when products are restocked

### Trade-in Process
1. Member submits device information online during purchase
2. Member brings device to customer service point
3. Officer inspects device and provides trade-in offer
4. Member can:
   - Accept offer → Order price adjusted, proceeds to shipment
   - Reject offer → Continue without trade-in OR cancel order
5. Trade-in discount cannot exceed order total amount

### Order Processing Rules
- Only in-stock products can be purchased
- Orders without trade-in: Direct processing by administrator
- Orders with trade-in: Requires officer approval before shipment
- Multiple devices can be traded in per order

## 🎓 Project Context

This project was developed as part of the ISOM3260/3760 course at HKUST (Hong Kong University of Science and Technology).

## 📝 License

This project is for educational purposes as part of coursework at HKUST.

---

**Note**: Database credentials shown in notebooks are for demonstration purposes. Update with your own credentials before running.

