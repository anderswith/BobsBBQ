# BobsBBQ

BobsBBQ is a web application for table reservations at a restaurant.
The system allows users to create an account, view the menu, and reserve tables within available time slots.

The project is developed with a focus on both backend functionality and DevOps practices, including automated testing, CI/CD, and deployment.

---

## Functionality

* User registration and login
* Password hashing with salt
* JWT-based authentication
* Table reservations within available time slots
* Display of the restaurant menu
* Email confirmation for:

  * Account creation
  * Table reservations
* Booking validation (prevent overlapping reservations)

---

## Technology

* C# / .NET (REST API)
* HTML frontend (wwwroot)
* MariaDB
* NUnit (unit tests)
* JWT authentication
* Email service

---

## DevOps

The primary focus of the project has been DevOps and automation.

### Containerization

* Docker for containerizing the application
* Docker Compose for orchestrating services (API + database)

### CI/CD Pipeline

The pipeline is implemented using GitHub Actions (YAML) and includes:

* Automatic build on push
* Running unit tests
* Code coverage
* Static code analysis with SonarQube
* Mutation testing with Stryker
* Performance/spike testing with k6

### Deployment

* The application is built as a Docker image
* The image is versioned and pushed to GitHub Container Registry
* Automatic deployment to a staging server (Oracle Cloud)
* Database migrations are applied to MariaDB

### Secrets and Configuration

* GitHub Secrets and variables are used to manage credentials and configuration in the pipeline

---

## Architecture

### Frontend

* HTML in wwwroot
* Communicates with the backend via HTTP requests

### Backend

* C# REST API
* Handles authentication, booking, and business logic

### Database

* MariaDB used for storing users, bookings, and related data
