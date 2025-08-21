# BoraViajar – Protótipo Full-Stack de Descoberta de Destinos

## Diagrama de Arquitetura

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
    end

    subgraph Backend
        B1[Controller - REST Endpoints]
        B2[Service - Lógica de Negócio]
        B3[Repository - JPA/Hibernate]
        B1 --> B2 --> B3
    end

    subgraph Database
        C1[Destinations Table]
        C2[Users Table]
        C1 --> C2
    end
