# PortfolioDB

**PortfolioDB** is a lightweight database manager for building and organizing a developer portfolio.  
It helps you store projects, associated skills, and track project status using SQLite.

---

## 🚀 Features

- Create and manage multiple projects
- Attach skills to each project
- Track project status (planning, in progress, completed, etc.)
- Supports multiple users
- Uses SQLite for easy and portable storage

---

## 🧱 Database Structure

The database includes four tables:

### `projects`
- `project_id` (Primary Key)
- `user_id`
- `project_name`
- `description`
- `url`
- `status_id` (Foreign Key)

### `skills`
- `skill_id` (Primary Key)
- `skill_name`

### `project_skills`
- `project_id` (Foreign Key)
- `skill_id` (Foreign Key)

### `status`
- `status_id` (Primary Key)
- `status_name`

---

## 🧠 How It Works

The `DB_Manager` class handles all database operations:

- Creating tables
- Inserting default skills and statuses
- Adding projects
- Linking skills to projects
- Retrieving project information
- Updating and deleting projects

---

## 🛠️ Installation

1. Clone the repository  
2. Install Python 3.8+  
3. Create a `config.py` file:

```python
DATABASE = "portfolio.db"
