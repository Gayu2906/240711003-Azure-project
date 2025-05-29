**LIBRARY MANAGEMENT SYSTEM(LMS)**
A scalable, cloud-based Library Management System built with Django (Python) for the backend and JavaScript for frontend interactivity. 
This application is deployed using Microsoft Azure App Service and integrated with GitHub Actions for continuous deployment.

**PROJECT OVERVIEW **
This web application allows users to manage a digital library system with features like
book cataloging, user authentication, issuing/returning books, and activity tracking.
It is designed to run on Azure cloud infrastructure with a focus on high availability, automation, 
and observability.

TECH STACK 










Layer	                                                                                                          Technology















 
Frontend	                                                                                                          HTML, CSS, JavaScript

















Backend	                                                                                                            Django (Python)




















 
Database                  	                                                                                       SQLite / Azure Database (configurable)





















Deployment                      	                                                                                 Azure App Service



















Static Hosting              	                                                                                 Azure Static Web Apps (for static assets)
























CI/CD Pipeline                  	                                                                           GitHub Actions

























Monitoring                                                                                                 	Azure Application Insights / Logs

AZURE SERVICES USED 



     1 Azure App Service – Hosts the Django web application.

     2 Azure Static Web Apps – Serves frontend assets (HTML, CSS, JS).

     3 Azure Monitor & Logs – Logs diagnostics and monitoring metrics.

     4 GitHub Actions – Automates build and deployment workflow.

 CORE FEATURES

      1 User authentication (admin and member roles)

      2 Book catalog (CRUD operations)

      3 Issue/return tracking with history logs

      4 Real-time search and filtering

      5 Admin dashboard with metrics

      6 Secured endpoints using Django middleware

      7 Deployment pipeline with rollback support

DEPLOYMENT WORKFLOW(CI/CD)


  1 This project uses GitHub Actions to automate the deployment process. The workflow:

  
  2  Triggers on push to the main branch.

  
  3 Installs dependencies and runs Django collectstatic.

  
  4 Deploys to Azure App Service via publishing profile secrets.

  
  5 Logs deployment success/failure.

   UML  DIAGRAMS

   USE CASE DIAGRAM 
   
   Shows the interactions between users (admin, member) and the system.

 ![use_case_diagram_half_size](https://github.com/user-attachments/assets/c5d94732-85d9-479a-960a-1fab57587217)


    CLASS DIAGRAM 
   
   Displays the data model (Book, User, IssueRecord, etc.).

   ![class_diagram_half_size](https://github.com/user-attachments/assets/b7bcc3d5-6e9e-4e8e-92d7-e64579998ad2)



   SEQUENCE DIAGRAM 
  
  Illustrates the flow of issuing a book.
  ![ChatGPT Image May 29, 2025, 01_46_28 PM](https://github.com/user-attachments/assets/1a16acdc-ae6f-486d-8afb-ae1fbf2cbcf5)


   ACTIVITY DIAGRAM
  
  Represents the user activity flow (e.g., login to book return).

  ![activity_diagram_half_size](https://github.com/user-attachments/assets/caf3794b-eb61-42ef-b487-9db5b20dac3b)


   DEPLOYMENT DIAGRAM 
  
  Visualizes how components are deployed in Azure (App Service, GitHub, Static Web App).

  ![ChatGPT Image May 29, 2025, 01_56_00 PM](https://github.com/user-attachments/assets/2b764ace-0fd4-49c8-ba84-475762719366)

**Architecture Diagram (Microservices)**

The system is designed using a Microservices Architecture, where each major functionality of the Library Management System is divided into independently deployable services.


![ChatGPT Image May 29, 2025, 04_39_59 PM](https://github.com/user-attachments/assets/08aba480-2d86-43a0-9441-cb504ee9de46)

 **Key Characteristics of Microservices**
 
**Independent Deployment**: Each service can be deployed or updated without affecting others.

**Technology Agnostic**: Different services can use different programming languages or databases.

**Scalability:** You can scale only the high-traffic services like Book Catalog independently.

**Resilience:** Failures in one service (e.g., Notifications) don't bring down the whole system.

**Maintainability:** Smaller codebases are easier to maintain and test

**Why Microservices for Library Management System?**

**Modularity:** A library system has well-defined modules (users, books, borrowing, etc.) which fit well into service boundaries.

**Team Autonomy: **Teams can develop and deploy each service independently (ideal for projects with multiple contributors).

**Future Scaling:** Microservices allow scaling specific parts (like Book Search) without overloading others (like Authentication).

**Continuous Delivery**: Faster deployment cycles using GitHub Actions CI/CD pipelines.

**Business Model Canvas**

Key Partners - Azure, Email Gateway, Library Networks, GitHub

key Activities - Book management, user engagement, issue/return tracking

Value Proposition -	Streamlined digital library operations, reduced manual work, 24x7 access

Customer Segments	- Students, Library Staff, Admins

Channels -	Web Interface, Email Alerts

Customer Relationships -	Automated interactions, Self-service

Revenue Streams -	Not applicable for free academic projects, 
but possible via subscription or fine management

Cost Structure -	Azure hosting, third-party APIs (e.g., for email/SMS)

![ChatGPT Image May 29, 2025, 04_45_29 PM](https://github.com/user-attachments/assets/7b9855de-691d-4533-a891-449b66aac7c3)


**SOLID Principles Applied**


**S –  Single Responsibility Principle**	Each service handles only one responsibility. Example: BookService handles only book-related logic.

****O –Open/Closed Principle**	**Easily extendable services using plug-ins or modules.

**L – Liskov Substitution Principle**	Interfaces and abstract classes ensure substitutable modules for things like notifications (email/SMS).

**I – Interface Segregation Principle**	Services expose only required interfaces via APIs.

**D – Dependency Inversion Principle** High-level modules (API Gateway) depend on abstractions, not concrete services.







 

 

 



