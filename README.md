# Inventory Management System

Inventory Management System is a full-stack application for managing IT assets, users, reports, and maintenance workflows. The repository contains the ASP.NET Core backend, the Angular frontend, and supporting class library projects used by the solution.

## Overview

This system is designed to help teams track inventory status, manage asset lifecycles, and monitor maintenance activity from a single application.

## Features

- Inventory tracking for available and faulty assets
- User management and role-based access support
- Asset lifecycle management from procurement to disposal
- Reports and analytics for operational visibility
- Maintenance scheduling and service history tracking
- Device status reporting

## Technology Stack

- Backend: ASP.NET Core
- Frontend: Angular
- Database: SQL Server

## Prerequisites

Before running the project, make sure the following are installed:

- .NET SDK 8.0 or higher
- Node.js 20.0 or higher
- Angular CLI 18.0 or higher
- SQL Server

## Repository Structure

- `InventrySystem/` - main backend application
- `InventryUI/` - Angular frontend application
- `Contracts/`, `Entities/`, `Repository/`, `Shared/`, `LoggerService/`, `EmailService/` - supporting projects and libraries

## Getting Started

### 1. Clone the Repository

```sh
git clone https://github.com/runehand/InventorySystem.git
cd InventorySystem
```

### 2. Configure the Database

Update the connection string in `appsettings.json` to match your SQL Server instance:

```json
"ConnectionStrings": {
  "sqlConnection": "server=.; database=InventrySystemDb; Integrated Security=true; TrustServerCertificate=true"
}
```

### 3. Run Database Migrations

The application uses Entity Framework Core Code First migrations.

1. Open the solution in Visual Studio.
2. Set `InventrySystem` as the default project in the Package Manager Console.
3. Run:

```powershell
Update-Database
```

### 4. Run the Backend API

Start the ASP.NET Core application. The API will be available at:

```text
https://localhost:5001/swagger/index.html
```

### 5. Run the Frontend

From the frontend directory:

```sh
cd InventrySystem/InventryUI
npm install
ng serve
```

The Angular app will be available at:

```text
http://localhost:4200
```

## Frontend Configuration

If needed, update the API endpoint in `src/environments/environment.ts`:

```typescript
export const environment = {
  production: false,
  apiUrl: 'https://localhost:5001'
};
```

## Default Login

The application includes a default administrator account for local testing.

- Username or email: `user@example.com`
- Password: `Password.123`

## Contributing

Contributions are welcome. If you plan to make changes, please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License.
