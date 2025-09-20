# Hospital Management System (HMS)

A relational database project designed to manage hospital operations efficiently—covering patients, doctors, nurses, appointments, payments, and research activities.

---

## 📋 Project Overview
The Hospital Management System aims to:
- Provide secure, centralized management of patient and doctor records.
- Automate patient registration and unique ID assignment.
- Allow appointment booking based on doctor availability.
- Enable online fee payments and prescription tracking.
- Restrict access to authorized personnel via secure login.
- Improve hospital operations and patient experience.

The database is **scalable** and ensures **data reliability** and **consistency**, with the potential for future feature expansion.

---

## 🏗️ Database Design

### Entities
- **Ward**
- **Employee** (Doctor, Nurse)
- **Research Lab**
- **Patient**
- **Admitted Patient**
- **Appointment**
- **Diagnosis**
- **Payment**

Each entity includes well-defined attributes and primary/foreign keys for data integrity.

### Relationships
- **One-to-many**: Nurse–Ward, Patient–Diagnosis, Patient–Payment, Patient–Appointment.
- **One-to-one**: Patient–Admitted Patient.
- **Many-to-many**: Doctor–Patient (via Appointment).
- **Weak Entity**: Research Lab linked to Doctor.

### Normalization
- All schemas satisfy **3NF** and **BCNF**.
- Some tables (e.g., `Nurse`, `Payment`) contain multi-value dependencies, breaching 4NF.

---

## 🗃️ Schema & Sample Tables
Core tables include:
- `Ward(Ward_No, Ward_Name, Floor_No)`
- `Doctor(Doctor_ID, First_Name, Last_Name, Gender, Specialty, Address, Salary)`
- `Nurse(Nurse_ID, First_Name, Last_Name, Gender, Ward_No, Type)`
- `Patient(Patient_ID, First_Name, Last_Name, Gender, DOB, Address, Contact_No)`
- `Appointment(Appointment_ID, Patient_ID, Doctor_ID, Appointment_Date_Time)`
- `Diagnosis(Diagnosis_ID, Appointment_ID, Patient_ID, Status, Follow_Up_Methods)`
- `Payment(Payment_ID, Appointment_ID, Mode_Of_Payment, Date_Time, Status, Location, Amount)`
- `Research_Lab(Research_ID, Doctor_ID, Research_Type)`

Refer to the project document for full SQL `CREATE TABLE` statements and example inserts.

---

## 🔎 Key SQL Queries
Sample operations included in the project:
- Retrieve patient details by address.
- Find doctors by gender or specialty.
- Book or cancel appointments.
- Calculate total payments by a patient.
- List nurses assigned to wards or patients.
- Identify doctors treating a specific illness.

---


## 👥 Authors
- **Saraf Abhinav Bala** (23CSB0A33)
- **Venneti Teja Sree Charan** (23CSB0A34)



