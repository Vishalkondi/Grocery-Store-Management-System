# 🛒 Grocery Store Management System (GSMS)

A Full Stack Grocery Store Management System built using HTML, CSS, JavaScript, Python Flask, and MySQL.

![GSMS Dashboard](./Screenshot%202026-06-01%20112840.png)

---

## 📌 Project Overview

The Grocery Store Management System helps store owners manage:

- Products
- Orders
- Inventory
- Revenue Tracking

This project demonstrates how modern full-stack applications are developed using frontend, backend, and database technologies.

---

## 🚀 Features

### Dashboard

- Modern responsive UI
- Grocery store banner
- Product statistics
- Order statistics
- Revenue tracking

### Product Management

- Add Products
- Delete Products
- View Product List
- Unit of Measurement (Kg, Litre, Piece)

### Order Management

- Create Orders
- Select Products
- Calculate Total Amount
- Store Orders in Database

### Backend APIs

- Get Products
- Add Products
- Delete Products
- Get Orders
- Create Orders
- Get UOM

---

## 🛠️ Tech Stack

### Frontend

- HTML5
- CSS3
- Bootstrap 5
- JavaScript
- jQuery

### Backend

- Python
- Flask

### Database

- MySQL

### Version Control

- Git
- GitHub

---

## 📂 Project Structure

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
├── README.md
└── homepage.JPG
```

---

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/Vishalkondi/Grocery-Store-Management-System.git
```

### Navigate to Project

```bash
cd Grocery-Store-Management-System
```

---

## 🗄️ MySQL Setup

Create Database:

```sql
CREATE DATABASE grocery_store;
USE grocery_store;
```

Create Tables:

### UOM Table

```sql
CREATE TABLE uom(
uom_id INT AUTO_INCREMENT PRIMARY KEY,
uom_name VARCHAR(50)
);
```

### Products Table

```sql
CREATE TABLE products(
product_id INT AUTO_INCREMENT PRIMARY KEY,
name VARCHAR(100),
uom_id INT,
price_per_unit DOUBLE
);
```

### Orders Table

```sql
CREATE TABLE orders(
order_id INT AUTO_INCREMENT PRIMARY KEY,
customer_name VARCHAR(100),
total DOUBLE,
datetime DATETIME
);
```

### Order Details Table

```sql
CREATE TABLE order_details(
order_id INT,
product_id INT,
quantity DOUBLE,
total_price DOUBLE
);
```

---

## 🔧 Configure Database

Update:

```python
backend/sql_connection.py
```

```python
host="localhost"
user="root"
password="YOUR_PASSWORD"
database="grocery_store"
```

---

## ▶️ Run Backend

Install Dependencies:

```bash
pip install flask
pip install flask-cors
pip install mysql-connector-python
```

Start Server:

```bash
cd backend
python server.py
```

Server:

```text
http://127.0.0.1:5000
```

---

## 🌐 Run Frontend

Open:

```text
ui/index.html
```

Recommended:

- Install Live Server Extension in VS Code
- Right Click → Open With Live Server

Frontend:

```text
http://127.0.0.1:5500
```

---

## 🔌 API Endpoints

### Get Products

```http
GET /getProducts
```

### Get UOM

```http
GET /getUOM
```

### Create Product

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

### Create Order

```http
POST /insertOrder
```

---

## 📸 Screenshots

### Dashboard

![Dashboard](./Screenshot%202026-06-01%20112840.png)

---

## 🎯 Learning Outcomes

This project demonstrates:

- Full Stack Development
- REST APIs
- Flask Backend
- MySQL Database Design
- CRUD Operations
- AJAX Requests
- Frontend & Backend Integration
- Git & GitHub Workflow

---

## 👨‍💻 Author

**Vishal Kondi**

- Full Stack Developer
- Frontend Developer
- React.js Developer
- Python Flask Developer

GitHub:

https://github.com/Vishalkondi

---

## ⭐ Support

If you found this project useful, please give it a ⭐ on GitHub.
