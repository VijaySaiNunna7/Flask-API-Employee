# Employee Management API (Flask)

## 📌 Overview

This project is a Flask-based REST API for managing and analyzing employee data. It provides endpoints to retrieve employee information, including filtering based on project status and bench allocation.

---

## 🚀 Features

* Retrieve all employee records
* Filter employees on bench
* Fetch employees working on active projects
* Fetch employees with completed projects
* Structured logging for API requests and responses
* Modular service-based architecture

---

## 🧠 Tech Stack

* **Backend:** Flask
* **Language:** Python
* **Data Handling:** JSON
* **Logging:** Custom logging module
* **Tools:** Postman

---

## ⚙️ API Endpoints

| Method | Endpoint                        | Description                           |
| ------ | ------------------------------- | ------------------------------------- |
| GET    | `/`                             | Health check                          |
| GET    | `/employees`                    | Get all employees                     |
| GET    | `/employees/bench`              | Get bench employees                   |
| GET    | `/employees/active_projects`    | Get employees with active projects    |
| GET    | `/employees/completed_projects` | Get employees with completed projects |

---

## ⚙️ How It Works

* Employee data is loaded from a JSON file during application startup
* Service layer processes and filters employee data
* API layer exposes endpoints for data retrieval
* Logging system tracks all requests and responses

The system logs initialization, request handling, and response details for monitoring and debugging .

---

## ▶️ Run the Application

```bash id="flaskrun"
pip install -r requirements.txt
python main.py
```

Server will start at:

```
http://127.0.0.1:5000/
```

---

## 📂 Project Structure

```id="emp123"
Employee-API/
│
├── main.py                      # Flask application entry point
├── app/
│   ├── service/
│   │   └── employee_service.py  # Business logic
│   ├── data/
│   │   └── employees_details.json
│   └── utils/
│       ├── logger.py
│       └── decorators.py
│
├── employee_api.log             # Application logs
├── requirements.txt
└── README.md
```

---

## 📊 Example Response

```json id="empjson"
{
  "emp_id": "E101",
  "name": "Vikram Deshmukh",
  "department": "Finance",
  "designation": "Analyst",
  "location": "Pune"
}
```

---

## ⚠️ Limitations

* Read-only API (no create/update/delete operations)
* Uses JSON file instead of database
* No authentication or authorization

---

## 🔮 Future Improvements

* Add CRUD operations
* Integrate database (PostgreSQL / MongoDB)
* Implement authentication (JWT)
* Add pagination and filtering

---

## 👨‍💻 Author

Vijay Sai Nunna
