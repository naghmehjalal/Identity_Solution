ASP.NET Core Identity Project (ASP.NET Core 8)

This project is a sample ASP.NET Core 8 web application demonstrating
how to implement authentication and role-based authorization using
ASP.NET Core Identity and Entity Framework Core.

Features

-   User Registration & Login via ASP.NET Core Identity
-   SMS Login support (Kavenegar API)
-   Google Account Authentication
-   Role-Based Authorization (Admin, User, Custom Roles)
-   Secure Access Control using [Authorize] + role checks
-   SQL Server integration through EF Core
-   Extendable Identity architecture for additional auth providers
-   Automatic creation of a default Administrator user (username:
    Administrator, password: P@ssword1) with full access during the
    first migration.

Technologies Used

-   ASP.NET Core 8 (MVC)
-   ASP.NET Core Identity
-   Entity Framework Core
-   Microsoft SQL Server
-   Google OAuth 2.0
-   Kavenegar API (SMS login)
-   Dependency Injection
-   GitHub Actions (optional CI/CD)

Getting Started

1. Clone the Repository

2. Configure the Database Connection

Update appsettings.json:

“ConnectionStrings”: { “DefaultConnection”: “YOUR_CONNECTION_STRING” }

3. Apply EF Core Migrations

dotnet ef database update
Running the migration will automatically create the default
Administrator user.

4. Configure External Logins

Google Login

“Authentication”: { “Google”: { “ClientId”: “YOUR_GOOGLE_CLIENT_ID”,
“ClientSecret”: “YOUR_GOOGLE_CLIENT_SECRET” } }

SMS Login (Kavenegar)

“Kavenegar”: { “ApiKey”: “YOUR_APIKEY”, “SenderNumber”:
“YOUR_SENDER_NUMBER” }
