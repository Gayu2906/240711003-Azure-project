LIBRARY MANAGEMENT SYSTEM(LMS)
A scalable, cloud-based Library Management System built with Django (Python) for the backend and JavaScript for frontend interactivity. 
This application is deployed using Microsoft Azure App Service and integrated with GitHub Actions for continuous deployment.

PROJECT OVERVIEW 
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

   ![ChatGPT Image May 29, 2025, 01_27_59 PM png](https://github.com/user-attachments/assets/ee4579ed-1784-4d91-ab1a-b495712d1c0b)

    CLASS DIAGRAM 
   
   Displays the data model (Book, User, IssueRecord, etc.).


   SEQUENCE DIAGRAM 
  
  Illustrates the flow of issuing a book. 

   ACTIVITY DIAGRAM
  
  Represents the user activity flow (e.g., login to book return).

   DEPLOYMENT DIAGRAM 
  
  Visualizes how components are deployed in Azure (App Service, GitHub, Static Web App).




 

 

 



