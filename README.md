# BoraViajar – Protótipo Full-Stack de Descoberta de Destinos

## Diagrama de Arquitetura
## Arquitetura Full-Stack

```mermaid
graph TD
    A[Frontend - Angular 18 SPA] -->|REST API| B[Backend - Java Spring Boot]
    B -->|JPA/Hibernate| C[Database - PostgreSQL]

    subgraph Frontend
        A1[Landing Page] 
        A2[Catálogo de Destinos] 
        A3[Cards Interativos]
        A4[Formulário de Contato]
        A1 --> A2 --> A3 --> A4
flowchart TB
    %% Frontend
    subgraph FE[Frontend - Angular 18 SPA]
        direction TB
        FE1[Landing Page]
        FE2[Catálogo de Destinos]
        FE3[Cards Interativos]
        FE4[Formulário de Contato]
        FE1 --> FE2 --> FE3 --> FE4
    end

    subgraph Backend
        B1[Controller - REST Endpoints]
        B2[Service - Lógica de Negócio]
        B3[Repository - JPA/Hibernate]
        B1 --> B2 --> B3
    %% Backend
    subgraph BE[Backend - Java Spring Boot]
        direction TB
        BE1[Controller - REST Endpoints]
        BE2[Service - Lógica de Negócio]
        BE3[Repository - JPA/Hibernate]
        BE1 --> BE2 --> BE3
    end

    subgraph Database
        C1[Destinations Table]
        C2[Users Table]
        C1 --> C2
    %% Database
    subgraph DB[Database - PostgreSQL]
        direction TB
        DB1[Destinations Table]
        DB2[Users Table]
        DB1 --> DB2
    end

    %% Integrações
    FE -->|HTTP REST API| BE
    BE -->|JPA/Hibernate| DB
