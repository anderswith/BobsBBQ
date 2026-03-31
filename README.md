# BobsBBQ

BobsBBQ er en webapplikation til bordbestilling for en restaurant.
Systemet gør det muligt for brugere at oprette en konto, se menuen og reservere borde inden for tilgængelige tidsperioder.

Projektet er udviklet med fokus på både backend-funktionalitet og DevOps-processer, herunder automatiseret test, CI/CD og deployment.

---

## Funktionalitet

* Oprettelse af bruger og login
* Password hashing med salt
* JWT-baseret authentication
* Bordbestilling inden for tilgængelige tidsrum
* Visning af restaurantens menu
* Email-bekræftelse ved:

  * Kontooprettelse
  * Bordreservation
* Validering af booking (undgå overlap)

---

## Teknologi

* C# / .NET (REST API)
* HTML frontend (wwwroot)
* MariaDB
* NUnit (unit tests)
* JWT authentication
* Email service

---

## DevOps

Projektets primære fokus har været DevOps og automatisering.

### Containerization

* Docker til containerisering af applikationen
* Docker Compose til at orkestrere services (API + database)

### CI/CD Pipeline

Pipeline er implementeret via GitHub Actions (YAML) og inkluderer:

* Automatisk build ved push
* Kørsel af unit tests
* Code coverage
* Statisk kodeanalyse med SonarQube
* Mutation testing med Stryker
* Performance/spike tests med k6

### Deployment

* Applikationen buildes som Docker image
* Image versioneres og pushes til GitHub Container Registry
* Automatisk deployment til staging server (Oracle Cloud)
* Database migration køres mod MariaDB

### Secrets og konfiguration

* GitHub Secrets og variables anvendes til håndtering af credentials og konfiguration i pipeline

---

## Arkitektur

### Frontend

* HTML i wwwroot
* Kommunikerer med backend via HTTP requests

### Backend

* C# REST API
* Håndterer authentication, booking og forretningslogik

### Database

* MariaDB til lagring af brugere, bookings og data
