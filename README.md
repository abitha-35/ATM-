

# 🏦 ATM Management System (Flask + MySQL Full Stack Project)

This is a full-stack **ATM Management System** developed using **Python (Flask)** for the backend, **MySQL** as the database, and **HTML/CSS** for the frontend interface. It simulates core banking functionalities such as withdraw, deposit, mini-statement, and PIN generation through a user-friendly web interface.

---

## 🔧 Tech Stack Used

* **Backend**: Flask (Python)
* **Frontend**: HTML, CSS (Responsive UI)
* **Database**: MySQL (pymysql connector)
* **Web Server**: Flask's built-in development server

---

## ✅ Features

### 🔐 PIN Generation

* Generate a new PIN using an account number
* Prevents PIN re-generation if one already exists
* Client-side validation with JavaScript alerts

### 💸 Withdraw

* Enter account number and PIN
* Check for valid account and sufficient balance
* Updates balance in the database after withdrawal

### 💰 Deposit

* Deposit money into an account using account number
* Automatically updates balance in MySQL

### 📄 Mini Statement

* Displays account details (name, email, balance) after validating PIN

### 🏠 Home Page

* Navigation to all services via modern card-style UI
* Classic UI with improved styling and responsive design

---

## 📁 Project Structure

```
project/
│
├── templates/
│   ├── home.html
│   ├── withdraw1.html, withdraw2.html
│   ├── deposit1.html
│   ├── ministatement1.html, ministatement2.html
│   ├── pingeneration1.html, pingeneration2.html
│
├── static/ (optional for CSS or JS)
│
├── app.py  ← Flask backend application
```

---

## 🗃️ Database Schema

**Table**: `ACCOUNTS`

| Column Name   | Type    | Description                  |
| ------------- | ------- | ---------------------------- |
| USER\_ACCNO   | VARCHAR | Account number (Primary Key) |
| USER\_NAME    | VARCHAR | Account holder's name        |
| USER\_EMAIL   | VARCHAR | Email of the user            |
| USER\_PIN     | INT     | 4-digit PIN                  |
| USER\_BALANCE | INT     | Current account balance      |

---

## 🚀 How to Run

1. **Clone the repo**

```bash
git clone https://github.com/your-username/atm-system.git
cd atm-system
```

2. **Set up a MySQL database**

* Create a database named `atm`
* Create the `ACCOUNTS` table with appropriate fields

3. **Install required Python packages**

```bash
pip install flask pymysql
```

4. **Run the Flask server**

```bash
python app.py
```


## 🔒 Security Notes

* For educational/demo purposes only. No encryption or production security features are implemented.
* Use environment variables for credentials if deploying.

---


## 📌 Future Enhancements

* Add login/authentication system
* Transaction history with timestamps
* Mobile responsive improvements
* Docker support for deployment

---


