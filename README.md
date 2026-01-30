# Database Modeling

A database design project for a school management system.

## Project Overview
This project implements a database design for YrkesCo, a vocational education provider operating schools in Stockholm and Göteborg. The system manages students, classes, programs, courses, teachers, and external consultants.

## Contents
- [Project Requirements](docs/project-requirements.md)
- [Conceptual ERD](docs/conceptual-model.md)
- [Logical ERD](docs/logical-model.md)
- [Physical ERD](docs/physical-model.md)
- [Physical model (DBML)](models/physical-model.dbml)
- [PostgreSQL schema](sql/schema.sql)
- [Sample queries](sql/queries.sql)
- [Sample data](sql/seed-data.sql)


## Database Features
- **15 tables** in 3NF
- **Constraints**: CHECK, FOREIGN KEY, UNIQUE, NOT NULL
- **Bridge tables** for many-to-many relationships
- **Sample records** for testing
- **JOIN queries** demonstrating relationships

## Setup (Getting started)
1. Clone the repo
```bash
    git clone https://github.com/aurabyte-dev/Database_Modeling_PostgreSQL.git
```

2. Copy `.env.example` to `.env` and add your own password
```bash
   cp .env.example .env
```

3. Start the Docker container
```bash
   docker compose up -d
```

4. Initialize the database schema
```bash
    docker exec -i postgres psql -U postgres -d myh_db < sql/schema.sql  
```

5. Load sample data
```bash
   docker exec -i postgres psql -U postgres -d myh_db < sql/seed-data.sql
```

To interact with the database:
```bash
docker exec -it postgres psql -U postgres -d myh_db
```

Database settings can be found in [docker-compose.yml](docker-compose.yml)

## Skills demonstrated
- Entity-Relationship Diagrams (ERD)
- Database normalization (3NF)
- PostgreSQL database design
- DBML
- Docker containerization
- Data integrity through constraints

