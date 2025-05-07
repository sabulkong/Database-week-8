# Clinic Booking System Database

## Description
This repository contains the SQL schema for a Clinic Booking System designed to manage departments, doctors, patients, appointments, and medical records. The database ensures data integrity with constraints, foreign keys, and indexes for efficient querying.

## Installation
1. **Prerequisites**: Ensure MySQL or MariaDB is installed.
2. Create a new database:
   ```sql
   CREATE DATABASE clinic_booking;
   USE clinic_booking;
   mysql -u [username] -p clinic_booking < db.sql
   Database Schema Overview
Tables
departments
Stores clinic departments.

Columns: department_id, name (unique), description.

doctors
Manages doctor details and their associated departments.

Columns: doctor_id, first_name, last_name, department_id (foreign key), contact_number (unique), email (unique), specialization.

patients
Stores patient information.

Columns: patient_id, first_name, last_name, date_of_birth, gender, contact_number (unique), email (unique), address.

appointments
Tracks patient appointments with doctors.

Columns: appointment_id, patient_id (foreign key), doctor_id (foreign key), appointment_date, appointment_time, status (Scheduled/Completed/Cancelled), created_at.

Unique constraint: A doctor cannot have overlapping appointments (same doctor_id, appointment_date, and appointment_time).

medical_records
Links to appointments and stores diagnostic information.

Columns: record_id, appointment_id (unique foreign key), diagnosis, prescription, notes,
record_date.

Indexes
Speed up queries on:

Patient names (idx_patient_name).

Doctor names (idx_doctor_name).

Appointment dates (idx_appointment_date).

