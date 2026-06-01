# 🛒 Grocery Store Management System (GSMS)

A Full Stack Grocery Store Management System built using HTML, CSS, JavaScript, Python Flask, and MySQL.

![GSMS Dashboard](homepage.JPG)

---

# 📌 Project Overview

The Grocery Store Management System helps store owners manage:

* 📦 Products
* 🛒 Orders
* 📊 Inventory
* 💰 Revenue Tracking

This project demonstrates how a complete software system is built using Frontend, Backend, APIs, and Database technologies.

---

# 🚀 Features

## Dashboard

* Modern Responsive UI
* Product Statistics
* Order Statistics
* Revenue Tracking
* Professional Admin Dashboard

## Product Management

* Add Products
* Delete Products
* View Product List
* Manage Product Units

## Order Management

* Create New Orders
* Select Multiple Products
* Calculate Total Amount
* Store Orders in Database

## Backend APIs

* Get Products
* Add Product
* Delete Product
* Get Orders
* Create Order
* Get Units of Measurement

---

# 🛠️ Tech Stack

## Frontend

* HTML5
* CSS3
* Bootstrap
* JavaScript
* jQuery

## Backend

* Python
* Flask

## Database

* MySQL

## Version Control

* Git
* GitHub

---

# 📂 Project Structure

```text
Grocery-Store-Management-System
│
├── backend
│   ├── server.py
│   ├── sql_connection.py
│   ├── products_dao.py
│   ├── orders_dao.py
│   └── uom_dao.py
│
├── ui
│   ├── index.html
│   ├── manage-product.html
│   ├── order.html
│   ├── css
│   ├── images
│   └── js
│
├── homepage.JPG
├── README.md
└── .gitignore
```

---

# ⚙️ Installation

## Clone Repository

```bash
git clone https://github.com/Vishalkondi/Grocery-Store-Management-System.git
```

## Navigate to Project

```bash
cd Grocery-Store-Management-System
```

---

# 🗄️ Database Setup

Create Database:

```sql
CREATE DATABASE grocery_store;
USE grocery_store;
```

### Create UOM Table

```sql
CREATE TABLE uom(
uom_id INT AUTO_INCREMENT PRIMARY KEY,
uom_name VARCHAR(50)
);
```

### Create Products Table

```sql
CREATE TABLE products(
product_id INT AUTO_INCREMENT PRIMARY KEY,
name VARCHAR(100),
uom_id INT,
price_per_unit DOUBLE
);
```

### Create Orders Table

```sql
CREATE TABLE orders(
order_id INT AUTO_INCREMENT PRIMARY KEY,
customer_name VARCHAR(100),
total DOUBLE,
datetime DATETIME
);
```

### Create Order Details Table

```sql
CREATE TABLE order_details(
order_id INT,
product_id INT,
quantity DOUBLE,
total_price DOUBLE
);
```

---

# 🔧 Configure Database

Update:

```text
backend/sql_connection.py
```

```python
host="localhost"
user="root"
password="YOUR_PASSWORD"
database="grocery_store"
```

---

# ▶️ Run Backend

Install Dependencies:

```bash
pip install flask
pip install flask-cors
pip install mysql-connector-python
```

Start Flask Server:

```bash
cd backend
python server.py
```

Server:

```text
http://127.0.0.1:5000
```

---

# 🌐 Run Frontend

Open:

```text
ui/index.html
```

Recommended:

* Install Live Server Extension
* Right Click → Open With Live Server

Frontend:

```text
http://127.0.0.1:5500
```

---

# 🔌 API Endpoints

### Get Products

```http
GET /getProducts
```

### Get UOM

```http
GET /getUOM
```

### Insert Product

```http
POST /insertProduct
```

### Delete Product

```http
POST /deleteProduct
```

### Get Orders

```http
GET /getAllOrders
```

### Insert Order

```http
POST /insertOrder
```

---

# 🎯 Learning Outcomes

This project demonstrates:

* Full Stack Development
* Flask REST APIs
* MySQL Database Design
* CRUD Operations
* AJAX Requests
* Frontend & Backend Integration
* Git & GitHub Workflow
* Real World Project Structure

---

# 👨‍💻 Author

**Vishal Kondi**

* Full Stack Developer
* Frontend Developer
* React Developer
* Python Flask Developer

GitHub:

https://github.com/Vishalkondi

---

# ⭐ Support

If you found this project useful, please give it a ⭐ on GitHub.
