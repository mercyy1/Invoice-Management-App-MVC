# 🧾 Invoice Management App (ASP.NET MVC)

Welcome to the **Invoice Management App**, a powerful, cleanly architected web application built using the **ASP.NET MVC Framework**. Designed for small to mid-sized businesses, this app simplifies how you manage your **clients, invoices, and customer records** — all in one intuitive interface.

---

## 🚀 Why This Project?

In a world flooded with complex ERP systems, this app brings **clarity and simplicity**. Whether you're a developer exploring MVC patterns or a business needing a minimal invoice tracker, this app offers:

- 👤 Clean customer management
- 📂 Categorized filtering (A–E, F–J, etc.)
- 🧠 MVC best practices with service abstraction
- 🎯 Razor-powered responsive UI
- 💬 Easily extensible for future features (e.g., invoice PDFs, payments, login)

---

## 🧩 Features

| Module                   | Description                                                            |
|--------------------------|------------------------------------------------------------------------|
| **Customer Manager**     | Add, edit, and filter customers by name ranges (e.g., A–E)             |
| **Dynamic Views**        | Razor-based UI rendering using ViewModels                              |
| **Service-Driven Logic** | Business logic abstracted via `IInvoiceManagerService`                 |
| **Clean Feedback**       | TempData-based alerts for user actions                                 |
| **Scalable**             | Built to plug in invoice, product, and authentication logic seamlessly |

---

## 🛠 Tech Stack

- **ASP.NET Core MVC** (.NET 8)
- **C#**
- **Razor Views**
- **Entity Framework Core** with **SQL Server** (migrations included)
- **Bootstrap** for styling
- **xUnit + Moq** for controller tests

---
## 🚀 Getting Started

### Prerequisites
- [.NET 8 SDK](https://dotnet.microsoft.com/download)
- Visual Studio 2022+ (or Rider, VS Code)

### Installation
```bash
git clone https://github.com/mercyy1/Invoice-Management-App-MVC.git
cd Invoice-Management-App-MVC
dotnet restore
dotnet ef database update --project InvoiceApp.DataAccess --startup-project InvoiceApp.Web
dotnet run --project InvoiceApp.Web
```

The connection string in `InvoiceApp.Web/appsettings.json` points at a local SQL Server (`Server=localhost`) using Windows authentication. Change it if your database runs elsewhere. The `dotnet ef` command (install with `dotnet tool install --global dotnet-ef`) creates the tables from the included migration.

Then open `http://localhost:5062/customers` in your browser (the port comes from `Properties/launchSettings.json`).

### Running the tests
```bash
dotnet test
```

---

## 📌 Usage Tips

* Navigate to `/customers` to view and manage customer records.
* Use `/customers/from_A-E` or other routes to filter customers alphabetically.
* Try adding and editing a customer to see validation and success alerts in action.

---

## 🧠 How It Works

Behind the scenes:

* `CustomerController` orchestrates routing and input.
* `IInvoiceManagerService` handles business logic, backed by Entity Framework Core and SQL Server.
* Razor Views render dynamic customer lists with categories.
* TempData ensures feedback persists across redirects.

---







