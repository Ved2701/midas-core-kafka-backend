# Midas Core – Event-Driven Transaction Processing System

A backend system built using Spring Boot, Apache Kafka, JPA/Hibernate, and REST APIs to process financial transactions asynchronously.

This project was completed as part of the JPMorgan Chase & Co. Software Engineering Job Simulation (Forage).

---

## Features

- Asynchronous transaction processing using Kafka
- Transaction validation (user existence & balance checks)
- Persistent storage using H2 database with JPA
- External Incentive REST API integration
- Atomic balance updates for sender and recipient
- REST API to query user balances
- Fully tested using embedded Kafka and in-memory database

---

## Tech Stack

- Java 17
- Spring Boot
- Apache Kafka
- Spring Data JPA / Hibernate
- H2 Database
- REST APIs
- Maven

---

## Architecture Overview

Kafka Producer  
↓  
Kafka Topic  
↓  
Midas Core (Kafka Consumer)  
↓  
Transaction Validation  
↓  
Database (H2 via JPA)  
↓  
Incentive API (REST)  
↓  
Updated User Balances  

---

## REST API

### Get User Balance

Endpoint:
GET /balance?userId={id}

Response:
{
  "amount": 1326.98
}

If the user does not exist:
{
  "amount": 0.0
}

---

## Testing

- Embedded Kafka for messaging tests
- In-memory H2 database for persistence
- Spring Boot integration tests

---

## Key Learnings

- Designing event-driven backend systems
- Kafka consumer configuration and message deserialization
- Handling transactional consistency in financial systems
- Integrating external REST APIs
- Debugging and validating distributed workflows

---

## Certificate

Completed as part of the JPMorgan Chase & Co. Software Engineering Job Simulation on Forage.

