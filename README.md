# 🖼️ ArtBase Database Design and SQL Project

This project showcases a fully designed and functional relational database system for **Art Galleries**, named **ArtBase**. It involves conceptual, logical, and physical design, and includes SQL queries, stored procedures, triggers, and a basic PHP-based data entry form.

---

## 📌 Project Overview

- **Project:** ArtBase – A Gallery-Oriented Relational Database
- **Objective:** Design and implement a normalized relational database to manage artists, artworks, customers, and art groups for gallery operations.
- **Tools Used:** SQL (T-SQL), XAMPP (PHP + MySQL), HTML/PHP for form interface

---

## 📂 Files Included

| File Name              | Description |
|------------------------|-------------|
| `report.docx`      | Complete written report with conceptual model, SQL schema, and queries |

---

## 🧱 Database Components

### 🧩 Entity Types
- **Artist** – Name, Birthplace, Age, Style of Art
- **Artwork** – Title, Type, Year, Price, Artist
- **Group** – Name
- **Customer** – Name, Address, Total Spent
- **CustomerPreferences** – Mapping between customers, artists, and groups

### 🔗 Relationships
- One-to-many: Artist ➝ Artwork  
- Many-to-many: Artwork ↔ Group, Customer ↔ Artist, Customer ↔ Group

---

## 🧠 Conceptual and Logical Design

- ER Diagram and EER Diagram included in report
- Tables with appropriate primary/foreign keys
- All tables normalized to **3rd Normal Form (3NF)**
- Functional Dependencies and assumptions clearly stated

---

## 🗃️ Tables & Schema

| Table Name            | Key Attributes |
|-----------------------|----------------|
| `Artists`             | `ArtistID (PK)` |
| `Artworks`            | `ArtworkID (PK)`, `ArtistID (FK)` |
| `Groups`              | `GroupID (PK)` |
| `Customers`           | `CustomerID (PK)` |
| `CustomerPreferences` | Composite PK: (`CustomerID`, `ArtistID`, `GroupID`) |

Additional features:
- `IDENTITY(1,1)` used for auto-increment IDs  
- `UNIQUE` and `NOT NULL` constraints used appropriately

---

## 🧾 SQL Functionality Implemented

### ✅ Basic SQL Queries
- `SELECT` queries with joins
- `INSERT INTO` new records
- `UPDATE` existing entries
- `DELETE` records
- Joining across multiple tables

### ⚙️ Advanced Features
- **Stored Procedure** – `AddNewArtwork` to insert new artwork
- **Trigger** – `UpdateTotalSpent` to update total spent after a purchase
- **Advanced Queries**:
  - Top spenders
  - Artworks in price range
  - Group search using `LIKE`
  - Customer preferences
  - Aggregate reports on artwork sales

---

## 🌐 Application (PHP Interface)

- **Technology Used:** XAMPP with PHP + MySQL
- Artist form created to add artist records into the database
- SQL `INSERT` statement used in PHP backend
- Form includes:
  - Name
  - Birthplace
  - Age
  - Style of Art

---

## 🚀 How to Run

1. Install **XAMPP** and start Apache + MySQL
2. Import SQL tables using the commands in the report
3. Place your PHP files inside `htdocs` (e.g., `htdocs/artbase`)
