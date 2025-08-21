# 🚀 BoraViajar – Protótipo Full-Stack de Descoberta de Destinos

Protótipo full-stack de plataforma web que conecta viajantes a destinos incríveis. Desenvolvido com **Angular 18 (SPA)** no frontend, **Spring Boot 3 + Java 17** no backend e **PostgreSQL** como banco de dados. Foco em escalabilidade, performance e UX.

---

## 🏗 Arquitetura do Sistema

```mermaid
flowchart LR
    %% Frontend ~30cm width
    subgraph FE[Frontend - Angular 18 SPA (~30cm)]
        direction TB
        FE1[Landing Page 6x2cm]
        FE2[Catálogo de Destinos 8x4cm]
        FE3[Cards Interativos 4x3cm]
        FE4[Formulário de Contato 6x3cm]
        FE1 --> FE2 --> FE3 --> FE4
    end

    %% Backend ~25cm width
    subgraph BE[Backend - Spring Boot REST API (~25cm)]
        direction TB
        BE1[Controller - Endpoints CRUD 6x2cm]
        BE2[Service - Business Logic 7x3cm]
        BE3[Repository - JPA/Hibernate 6x3cm]
        BE1 --> BE2 --> BE3
    end

    %% Database ~15cm width
    subgraph DB[Database - PostgreSQL (~15cm)]
        direction TB
        DB1[destinations: id, name, description, price, image_url, location 5x3cm]
        DB2[users: id, name, email, message, created_at, updated_at 5x3cm]
        DB1 --> DB2
    end

    %% Integrações
    FE -->|HTTP REST API| BE
    BE -->|JPA/Hibernate| DB
