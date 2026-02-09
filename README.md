# Bash DBMS Simulator (GUI with Zenity)

A lightweight **Database Management System simulator** built using **Bash scripting** and **Zenity** for the graphical interface.

This project mimics core DBMS operations (like MySQL basics) but uses the **file system** as storage and **shell scripting** as the engine.

It is designed for **educational purposes** to understand how databases work internally.

## 🎯 Project Goal

To simulate fundamental database concepts using:

- 🐚 Bash scripting (application logic)
- 🖥️ Zenity (GUI dialogs)
- 📁 Linux file system (data storage)

This project helps in understanding:

- Database structure
- Table management
- CRUD operations
- How DBMS systems organize and manipulate data internally

## 🧱 System Architecture

```bash
Database  →  Directory
Table     →  File
Record    →  Line in file
Field     →  Value separated by delimiter
```

## 🛠 Requirements

Make sure the following are installed:

| Tool   | Purpose              |
| ------ | -------------------- |
| Bash   | Script execution     |
| Zenity | GUI dialogs          |
| Linux  | File system handling |

### Install Zenity (if missing)

```bash
sudo apt install zenity
```

### How to Run

```bash
chmod +x main.sh
./main.sh
```

## App Flow

The program is menu-driven and divided into three main levels.

### 1️⃣ Main Menu

Appears when the program starts.

| Option               | Description                          |
| -------------------- | ------------------------------------ |
| **Create Database**  | Creates a new database (directory)   |
| **List Databases**   | Shows all existing databases         |
| **Connect Database** | Choose a database to work with       |
| **Drop Database**    | Delete a database and all its tables |
| **Exit**             | Close the application                |

### 2️⃣ Database Selection Menu

After choosing Connect Database, the system displays all databases so the user can select one to work on.

### 3️⃣ Table Operations Menu (Inside a Database)

Each database has its own menu (handled by a separate script file).

| Option                | Description                               |
| --------------------- | ----------------------------------------- |
| **Create Table**      | Creates a table file with defined columns |
| **List Tables**       | Displays tables in the selected database  |
| **Drop Table**        | Deletes a table file                      |
| **Insert Into Table** | Adds a new record                         |
| **Select From Table** | View records with different options       |
| **Delete From Table** | Remove specific records                   |
| **Update Entry**      | Modify existing data                      |
| **Back to Main Menu** | Return to main menu                       |
| **Exit**              | Close the program                         |

### 📋 Table Structure

When creating a table, the user defines:

- Table name
- Number of columns
- Column names
- Data is stored in this format:

```bash
id:name:age:city
1:Ali:22:Cairo
2:Sara:25:Giza
```

Delimiter used: `:` (can be changed in the script)

## 🔍 Features

- ✅ GUI interface using Zenity
- ✅ Multiple databases support
- ✅ Multiple tables per database
- ✅ Insert / Select / Update / Delete records
- ✅ Data validation (name rules, existence checks)
- ✅ Separate script for table operations
- ✅ Simulates real DBMS workflow

## ⚙️ Internal Logic

| DBMS Concept     | Bash Implementation  |
| ---------------- | -------------------- |
| Database         | Directory            |
| Table            | Text file            |
| Schema           | First row of file    |
| Record           | Line in file         |
| Query processing | `awk`, `sed`, `grep` |
| GUI Interaction  | Zenity dialogs       |

## 👨‍💻 Author

Developed as a learning project to understand DBMS fundamentals using Linux shell scripting.

If you want, next we can make:  
📁 project folder structure section or  
🧠 internal script design explanation (how each function works).
