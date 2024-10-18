__Purpose__
This project is a web-based eCommerce platform built using ASP.NET Core MVC with Entity Framework (EF) Core for database management. The system offers robust user role management, including admin,producers and consumers, each with specific functionalities. The platform supports product management, user profile handling, and order management workflows with CRUD operations across all roles.

__Features__
Role-based Authorization

Producers: Manage product catalogs (add, update, delete products).
Consumers: Place orders, manage profiles, and view products.
Entity Framework Core

-Database operations are managed through EF Core, providing ORM functionalities.
Uses Migrations to ensure smooth schema updates.
State Management & Sessions

-User authentication and authorization managed using sessions.
Different session states for logged-in and guest users.
CRUD Operations

-Products and user profiles support full Create, Read, Update, and Delete operations.
Products can be searched and filtered by name, date, and price.
Order Management System

-Orders progress through the following statuses:
Pending: Booked but payment pending.
Confirmed: Payment received.
Dispatched: Order in transit.
Finished: Delivered and payment completed.
Canceled: Order can be cancelled also by consumer.
Notifications

-Email notifications for order status updates.

-Responsive Design & User-friendly Interface
Fully responsive UI for a seamless experience across devices.

-Uses ASP.NET Core Identity for authentication.
Composite keys applied to UserID and Email to ensure data integrity.

-__Technologies Used__
ASP.NET Core MVC
Entity Framework Core
Microsoft SQL Server
Bootstrap 5 / CSS for frontend styling
Session Management for state handling
ASP.NET Core Identity for authentication
Payment Management: strip
Email sending: sendGrid


__To run the project steps__

__Prerequisites__
Before running the project, ensure the following tools are installed:

.NET SDK (matching your project version)
SQL Server (or any configured database)
Visual Studio (or any IDE with .NET Core support)
Entity Framework Core CLI (installed via .NET CLI)
dotnet tool install --global dotnet-ef
Account on sendGrid

__Steps to Run the Project__

1.Navigate to the project folder in the terminal

2. Configure the Database
Open appsettings.json and ensure the connection string to the SQL database is correctly configured.

3. Apply Migrations
If the project uses EF Core migrations, you need to apply them:
dotnet ef database update
This command creates the database and applies the latest migration to set up the schema.

4. Build the Project
Run the following to compile the code and check for errors:
dotnet build

5. Run the Application
Launch the web application using the command:
dotnet run
This starts the server on the default localhost

5. Open in Browser
After the application starts, you will see the terminal output with the URL (e.g., http://localhost:portno).
Open the URL in a web browser to access the website.
