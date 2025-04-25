# Contact Manager with Authentication & Authorization in ASP.NET Core

This ASP.NET Core web application provides a contact management system with robust user authentication and authorization. It implements role-based access control to ensure data is accessed and managed securely.

## Project Description

The application allows users to create and manage contact information. Access to this information is restricted based on the user's role within the system.  The system defines three security groups:

* **Registered Users:** Can view and edit/delete their own contact data. [cite: 137, 138, 139, 144, 145]
* **Managers:** Can approve or reject contact data. [cite: 137, 138, 139, 146, 147]
* **Administrators:** Have full access to approve/reject and edit/delete any data within the system. [cite: 137, 138, 139, 148, 149]

## Features

* **User Authentication:** Secure user registration and login functionality. [cite: 137, 156, 157, 158, 159]
* **Role-Based Authorization:** Implementation of roles (Registered User, Manager, Administrator) and policies to control access to data and actions. [cite: 142, 143]
* **Contact Data Management:**
    * Create, read, update, and delete contact information.
    * Users can manage their own contact data. [cite: 144, 145]
    * Managers can approve or reject contact submissions. [cite: 146, 147]
    * Administrators have full control over contact data. [cite: 148, 149]
* **Data Storage:** The application uses a database to persist contact information. [cite: 147]

## Technologies Used

* ASP.NET Core
* C#
* ASP.NET Core Identity (for authentication and authorization)
* Entity Framework Core (for database interaction - likely SQL Server, based on the code)
* HTML/CSS/JavaScript (for the user interface)

## Setup Instructions

1.  **App Setup:** Follow the instructions in the provided tutorial to set up the ASP.NET Core application. [cite: 141] This will involve configuring the database connection and other application settings. [cite: 150, 151, 152, 153]
2.  **Database Configuration:** Ensure you have a SQL Server instance available and update the connection string in `appsettings.json`.
3.  **User Secrets:** The application uses user secrets to store sensitive information like passwords.  Use the `dotnet user-secrets` command-line tool to set the password for the seed user. [cite: 150, 151, 152, 153, 154]
4.  **Apply Migrations:** Use Entity Framework Core migrations to create the database schema.
5.  **Run the Application:** Build and run the ASP.NET Core application.

##  Important Notes

* The application implements security best practices, including authentication and role-based access control.
* The "Powerpoint Presentation.pdf" document provides additional context and details about the project's goals and implementation.

##  Security Considerations (From "Powerpoint Presentation.pdf")

The "Powerpoint Presentation.pdf" document also discusses broader security considerations for data transfer and API security:

* **Secure Data Transfer:** Recommendations for secure data transfer within a network include using VPNs, SSL/TLS, SFTP, and encrypted email. [cite: 173, 174, 175, 176, 177, 178, 179, 180, 181, 182, 183, 184, 185, 186, 187, 188, 189, 190]
* **Secure API Architecture:** The document outlines the key components of a secure API, including authentication, authorization, encryption (HTTPS/SSL), and security monitoring. [cite: 202, 203, 204, 205, 206, 207, 208, 209, 210, 211, 212, 213, 214, 215, 216, 217, 218, 219, 220, 221, 222, 223, 224, 225, 226, 227, 228]
* **Data Interchange Format:** JSON and XML are discussed as suitable data interchange formats, balancing security, interoperability, and efficiency. [cite: 229, 230, 231, 232, 233, 234, 235, 236, 237, 238, 239, 240, 241]
* **Data Storage:** Distributed database systems are recommended for storing data across multiple locations, with considerations for sharding and replication. [cite: 242, 243, 244, 245, 246, 247, 248, 249, 250, 251, 252]
* **Ethical Concerns:** The document highlights the ethical considerations surrounding the transmission of personal data, emphasizing the importance of data breach prevention, responsible data use, user rights, and protection of vulnerable populations. [cite: 253, 254, 255, 256, 257, 258, 259, 260, 261, 262, 263, 264, 265]
