#  Hospital Management App

A **Flask-based web application** for managing hospital operations — including **user authentication**, **doctor approvals**, **patient registration**, and **appointment scheduling** — all powered by a lightweight **SQLite** database.

---

## 🚀 Features

- 👩‍⚕️ **Admin Dashboard**
  - Add doctors with department and specialization
  - View all patients and appointments
  - Manage doctor approvals and access

- 🧑‍⚕️ **Doctor Dashboard**
  - View upcoming appointments
  - Complete consultations with diagnosis and prescription entry
  - Access appointment history

- 🧑‍💻 **Patient Dashboard**
  - Self-registration and secure login
  - Browse available doctors
  - Book appointments with time-slot conflict checking

- 🧩 **Appointment Management**
  - Start and end time validation
  - Prevention of overlapping appointments
  - Status tracking (`Booked`, `Completed`)

- 🔐 **Secure Authentication**
  - Passwords hashed using `werkzeug.security`
  - Role-based access (`admin`, `doctor`, `patient`)
  - Session-based login via `Flask-Login`

- 🧱 **Modular Architecture**
  - SQLAlchemy ORM models
  - Blueprints for clean route separation
  - Jinja2 + Bootstrap frontend

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-------------|
| Backend | Flask (Python) |
| Database | SQLite (via SQLAlchemy ORM) |
| Frontend | HTML5, CSS3, Bootstrap, Jinja2 Templates |
| Forms & Validation | Flask-WTF, WTForms |
| Authentication | Flask-Login |
| Migration | Flask-Migrate |
| Password Security | Werkzeug Hashing |

---

## 🧩 Project Structure

hospital_management_app/
│
├── app/
│   ├── __init__.py          # App factory, DB & Login setup
│   ├── models.py            # SQLAlchemy ORM models
│   ├── routes.py            # Flask routes & forms
│   ├── templates/           # HTML templates (Bootstrap + Jinja2)
│   └── static/              # CSS / JS / assets
│
├── instance/
│   └── hospital.db          # SQLite database (auto-created)
│
├── create_db.py             # Database utility (init/reset/admin)
├── requirements.txt         # Python dependencies
└── README.md                # Project documentation


⚙️ Installation & Setup
Prerequisites

Python 3.10 or newer

Virtual environment (recommended)
steps
# 1️⃣ Clone the repository
git clone [https://github.com/SHIN-1O1/Hospital_Management_App.git](https://github.com/SHIN-1O1/Hospital_managment_app.git)
cd Hospital_Management_App

# 2️⃣ Create & activate a virtual environment
python -m venv venv
venv\Scripts\activate        # on Windows
# source venv/bin/activate   # on Mac/Linux

# 3️⃣ Install dependencies
pip install -r requirements.txt

# 4️⃣ Initialize the database
python create_db.py --init

# 5️⃣ Run the Flask app
flask run



