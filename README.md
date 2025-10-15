
# 🏥 Clinic Booking System — Database Project

## 📌 Overview
This project implements a full-featured **relational database** for a Clinic Booking System using **MySQL**. It models real-world clinic operations including patient registration, doctor assignment, appointment scheduling, and prescription management.

## 🎯 Objectives
- Design a normalized relational schema with appropriate constraints.
- Implement relationships: One-to-One, One-to-Many, and Many-to-Many.
- Provide a scalable foundation for clinic operations and future integration with applications.

## 🗂️ Schema Summary

| Table                    | Description                                      |
|-------------------------|--------------------------------------------------|
| `Departments`           | Stores clinic departments (e.g., Cardiology)     |
| `Doctors`               | Doctor profiles linked to departments            |
| `Patients`              | Patient records with contact and DOB info        |
| `Appointments`          | Scheduled visits between patients and doctors    |
| `Prescriptions`         | One-to-one link to appointments with notes       |
| `Medications`           | Medication catalog                               |
| `Prescription_Medications` | Many-to-many link between prescriptions and medications |

## 🔗 Relationships
- **One-to-Many**: Departments → Doctors, Patients → Appointments, Doctors → Appointments
- **One-to-One**: Appointments → Prescriptions
- **Many-to-Many**: Prescriptions ↔ Medications

## 📄 File Structure
- `clinic_schema.sql`: Contains all SQL statements to create the database and tables with constraints.

## 🚀 How to Use

1. **Setup MySQL**
   - Ensure MySQL is installed and running.
   - Use a MySQL client (e.g., MySQL Workbench, VS Code extension, or CLI).

2. **Run the SQL Script**
   ```bash
   mysql -u your_username -p < clinic_schema.sql
   ```

3. **Verify Tables**
   ```sql
   USE ClinicDB;
   SHOW TABLES;
   ```

4. **Insert Sample Data (Optional)**
   You can extend the script with `INSERT INTO` statements to populate the tables.

## ✅ Constraints Used
- `PRIMARY KEY` for unique identification
- `FOREIGN KEY` for relational integrity
- `NOT NULL` to enforce required fields
- `UNIQUE` to prevent duplicate entries (e.g., emails)

## 📌 Future Enhancements
- Add user authentication for doctors and staff
- Build a front-end interface (e.g., Flask or Django)
- Integrate billing and insurance modules

## 👨‍💻 Author
Victor Mwenda — Entrepreneur, student, and family leader  
Focused on practical technical learning and community impact

