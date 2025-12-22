# Income & Expenses Tracker

A Windows desktop application for tracking personal income and expenses, built with **C# WinForms** on **.NET Framework 4.7.2** and backed by **SQL Server LocalDB**.

<!-- Add a screenshot: put an image in a docs/ folder and uncomment the line below -->
<!-- ![Dashboard](docs/dashboard.png) -->

## Features

- **Accounts**: registration and login
- **Dashboard**: income and expense totals for today, yesterday, this month, this year and all time
- **Categories**: create, edit and deactivate income and expense categories
- **Income & expenses**: add, update and delete entries, each with a category, amount, description and date
- All queries are parameterized

## Tech stack

| Layer | Technology |
|---|---|
| UI | Windows Forms (C#) |
| Runtime | .NET Framework 4.7.2 |
| Database | SQL Server LocalDB (`System.Data.SqlClient`) |

## Getting started

### Prerequisites

- Windows with Visual Studio 2019 or later (".NET desktop development" workload, which includes LocalDB)

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/IhebMessaadia/IncomeExpensesTracker.git
   ```
2. Create the database: in Visual Studio, open **SQL Server Object Explorer**, add a new database on `(LocalDB)\MSSQLLocalDB`, and run [`database/schema.sql`](database/schema.sql) against it.
3. Update the connection string in the forms (search for `Data Source=`) so that `AttachDbFilename` points to your `.mdf` file.
4. Open `src/IncomeExpensesTrackingManagementSystem.sln` and press **F5**.

## Project structure

```
database/
└── schema.sql                  # Tables: users, categories, income, expenses
src/
├── IncomeExpensesTrackingManagementSystem.sln
└── IncomeExpensesTrackingManagementSystem/
    ├── Form1.cs                # Login
    ├── RegisterForm.cs         # Sign-up
    ├── MainForm.cs             # Main window and navigation
    ├── DashboardForm.cs        # Totals by day, month and year
    ├── CategoryForm.cs         # Category management
    ├── IncomeForm.cs           # Income entries
    ├── ExpensesForm.cs         # Expense entries
    ├── *Data.cs                # Data access classes
    └── Assets/                 # Icons
```

## Author

**Iheb Messaadia**: [GitHub](https://github.com/IhebMessaadia)
