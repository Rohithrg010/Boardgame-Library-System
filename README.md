# Boardgame Library System (NoSQL – MongoDB)

## 📌 Project Overview
This project implements a **Board Game Library and Lending System** using **MongoDB** to demonstrate NoSQL data modeling techniques.  
It simulates a real-world board game lending system where users can borrow and return games, similar to a traditional library.

The project explores multiple **NoSQL design patterns** to handle one-to-many relationships efficiently while enforcing business rules.

---

## 👥 Team Members
- **Rohith Gowda Ranganatha**
- **Kavit Mehta**

---

## 🛠️ Technologies Used
- MongoDB
- JSON Schema Validation
- MongoDB Compass
- NoSQL Data Modeling

---

## 📂 Database Designs Implemented

### 🔹 Design 1: `user_active_loans` (Array)
- Stores a user's active loan IDs as an array
- Enforces a maximum of **3 active loans per user**
- Prevents infinite array growth using business rules

### 🔹 Design 2: `users_with_loans` (Embedded Subdocuments)
- Embeds loan documents directly inside each user
- Tracks loan dates and return status
- Ensures users cannot exceed active loan limits

### 🔹 Design 3: `boardgames_with_borrowers` (Array of Subdocuments)
- Stores all active borrowers for a given board game
- Removes borrower records once a loan is returned
- Prevents infinite document growth

---

## 📑 JSON Schema Validation
JSON Schema is used to:
- Enforce data integrity
- Validate required fields
- Apply business constraints such as:
  - Minimum string lengths
  - Positive numeric values
  - Maximum array sizes
  - No duplicate loan IDs

---

## 🔍 Sample Queries Implemented
- Find games with borrowers having `loan_id > 15`
- Find users with exactly **2 active loans**
- Find users with at least one returned loan
- Query within arrays and embedded documents

---

## 📁 Repository Structure
