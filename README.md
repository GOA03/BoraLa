# BoraViajar – Protótipo Full-Stack de Descoberta de Destinos

## Arquitetura Full-Stack

```mermaid
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

    %% Backend
    subgraph BE[Backend - Java Spring Boot]
        direction TB
        BE1[Controller - REST Endpoints]
        BE2[Service - Lógica de Negócio]
        BE3[Repository - JPA/Hibernate]
        BE1 --> BE2 --> BE3
    end

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
