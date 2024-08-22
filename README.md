# Blazor-CarInventoryDataGrid
This project is a simple car inventory management system built using Blazor and Radzen components. It provides functionality to view, add, edit, and delete car records from the inventory.

This was built using the principles of clean architecture as it applies to the onion architecture, top-down dependency management, and modular monolith applications.

Blazor applications built in this fashion are good candidates for reusable libraries, developing in team settings, and increasing testability and reusability of code. 

# Feature
- **Radzen DataGrid:** A powerful data grid with features like filtering, sorting, and paging.
- **Dialog Service:** Used to display dialogs for adding and editing car records.
- **Car Service:** A service layer to manage CRUD operations for car data.

## Prerequisites
Before running this project, ensure you have the following:

- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0) installed.
- [Radzen.Blazor](https://www.nuget.org/packages/Radzen.Blazor) package installed.

## Project Structure
- **CarInventoryDataGrid.Domain:** Contains the `CarEntity` class representing the car entity.
- **CarInventoryDataGrid.Models:** (Optional) Contains additional models or DTOs.
- **CarInventoryDataGrid.Services:** Contains the `ICarService` interface and its implementation for CRUD operations.

## Getting Started

### 1. Set up the Database
Create the `CarInventory` table using the SQL script below:


CREATE TABLE CarInventory (
    Id INT PRIMARY KEY IDENTITY(1,1),
    Make NVARCHAR(50) NOT NULL,
    Model NVARCHAR(50) NOT NULL,
    Year INT NOT NULL,
    Price DECIMAL(18, 2) NOT NULL,
    Engine NVARCHAR(50) NOT NULL,
    Color NVARCHAR(50) NOT NULL
);


### 2. Insert Sample Data

INSERT INTO CarInventory (Make, Model, Year, Price, Engine, Color)
VALUES ('Toyota', 'Camry', 2020, 24999.99, '2.5L I4', 'White');

INSERT INTO CarInventory (Make, Model, Year, Price, Engine, Color)
VALUES ('Honda', 'Civic', 2019, 19999.99, '2.0L I4', 'Black');

INSERT INTO CarInventory (Make, Model, Year, Price, Engine, Color)
VALUES ('Ford', 'Mustang', 2022, 35999.99, '5.0L V8', 'Red');

INSERT INTO CarInventory (Make, Model, Year, Price, Engine, Color)
VALUES ('Tesla', 'Model S', 2021, 79999.99, 'Electric', 'Blue');

INSERT INTO CarInventory (Make, Model, Year, Price, Engine, Color)
VALUES ('Chevrolet', 'Silverado', 2023, 44999.99, '6.2L V8', 'Silver');

### 3. Configure Connectionstring in appsettings.json file


## Run Application
- Open the project in your favorite IDE (e.g., Visual Studio, Visual Studio Code).
- Restore the NuGet packages.
- Build and run the application.
