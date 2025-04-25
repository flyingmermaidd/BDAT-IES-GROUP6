# Contact Manager with Authentication & Authorization in ASP.NET Core

This ASP.NET Core web application provides a contact management system with user authentication and role-based access control.

## Project Description

The application allows users to create and manage contact information. Access to this information is restricted based on the user's role within the system. The system defines three security groups:

* **Registered Users:** Can view and edit/delete their own contact data.
* **Managers:** Can approve or reject contact data.
* **Administrators:** Have full access to approve/reject and edit/delete any data within the system.

## Features

* **User Authentication:** Secure user registration and login functionality using ASP.NET Core Identity.
* **Role-Based Authorization:** Implementation of roles (Registered User, Manager, Administrator) and policies to control access to data and actions.
* **Contact Data Management:**
    * Create, read, update, and delete contact information.
    * Users can manage their own contact data.
    * Managers can approve or reject contact submissions.
    * Administrators have full control over contact data.
* **Data Storage:** Uses a database (SQL Server, as indicated by the code) to persist contact information.

## Technologies Used

* ASP.NET Core
* C#
* ASP.NET Core Identity (for authentication and authorization)
* Entity Framework Core (for database interaction - likely SQL Server, based on the code)
* HTML/CSS/JavaScript (for the user interface)

## Repository Structure

The repository has the following structure:

```
ContactManager/
├── final6/                     # Contains the ASP.NET Core web application project.
│   ├── .vs/                    # Visual Studio solution settings (not essential for building)
│   ├── ContactManager/         # The main ASP.NET Core project directory
│   │   ├── Areas/Identity/Pages/  # ASP.NET Core Identity pages
│   │   ├── Authorization/       # Authorization handlers and related files
│   │   ├── Data/                # Entity Framework Core database context and migrations
│   │   ├── Models/              # Data models (e.g., Contact.cs)
│   │   ├── Pages/               # Razor Pages for the application's UI
│   │   ├── Shared/              # Shared layout and error pages
│   │   ├── Properties/          # Project properties
│   │   ├── bin/                 # Compiled binaries
│   │   ├── obj/                 # Intermediate build objects
│   │   ├── wwwroot/             # Static web assets (CSS, JavaScript, images)
│   │   ├── appsettings.json     # Application configuration
│   │   ├── appsettings.Development.json # Development-specific configuration
│   │   ├── ContactManager.csproj # Project file
│   │   ├── ContactManager.sln  # Solution file
│   │   ├── Program.cs           # Application entry point
│   └── ... (other files)
├── Powerpoint Presentation.pptx  # Presentation slides for the project
├── Powerpoint Presentation.pdf  # Presentation slides for the project in pdf format
└── README.md                  # This file
```

## Setup Instructions

1.  **Prerequisites:**
    * Ensure you have the .NET Core 6.0 SDK installed.
    * A SQL Server instance is required for the database.

2.  **Database Configuration:**
    * Update the connection string in `final6/ContactManager/appsettings.json` to point to your SQL Server.

3.  **User Secrets:**
    * Use the `dotnet user-secrets` command-line tool within the `final6/ContactManager` directory to set the password for the seed user (if applicable, as mentioned in "Final Project.pdf").  Example: `dotnet user-secrets set "SeedUserPW" "YourSecurePassword"`

4.  **Apply Migrations:**
    * Open a terminal in the `final6/ContactManager` directory and run the following commands:
        * `dotnet build`
        * `dotnet ef database update`

5.  **Run the Application:**
    * Execute `dotnet run` from the `final6/ContactManager` directory to start the application.

##  Important Notes

* The application implements security best practices, including authentication and role-based access control.
* The `Powerpoint Presentation` document provides additional context and details about the project's goals and implementation.

##  Security Considerations (From "Powerpoint Presentation")

The "Powerpoint Presentation.pdf" document also discusses broader security considerations for data transfer and API security:

* **Secure Data Transfer:** Recommendations for secure data transfer within a network include using VPNs, SSL/TLS, SFTP, and encrypted email.
* **Secure API Architecture:** The document outlines the key components of a secure API, including authentication, authorization, encryption (HTTPS/SSL), and security monitoring.
* **Data Interchange Format:** JSON and XML are discussed as suitable data interchange formats, balancing security, interoperability, and efficiency.
* **Data Storage:** Distributed database systems are recommended for storing data across multiple locations, with considerations for sharding and replication.
* **Ethical Concerns:** The document highlights the ethical considerations surrounding the transmission of personal data, emphasizing the importance of data breach prevention, responsible data use, user rights, and protection of vulnerable populations.
