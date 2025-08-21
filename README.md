# 🚀 BoraViajar – Protótipo Full-Stack de Descoberta de Destinos

Protótipo full-stack de plataforma web que conecta viajantes a destinos incríveis. Desenvolvido com **Angular 18 (SPA)** no frontend, **Spring Boot 3 + Java 17** no backend e **PostgreSQL** como banco de dados. Foco em escalabilidade, performance e UX.

---

## 🏗 Arquitetura do Sistema (medidas aproximadas em cm)

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

✨ Funcionalidades

Frontend (Angular 18 SPA)

Landing Page responsiva (Hero, About Us, Benefits, CTA)

Catálogo de Destinos: Grid de cards com imagens, descrição e preço

Cards interativos com animações suaves

Formulário de contato com validação e envio via API

SEO otimizado

Backend (Spring Boot REST API)

Controller: CRUD endpoints (/api/destinations)

Service: Lógica de negócio, validações

Repository: JPA/Hibernate

Database (PostgreSQL)

destinations e users com campos principais para protótipo

⚡ Tecnologias

Frontend: Angular 18, TypeScript, Angular Material, SCSS, RxJS
Backend: Spring Boot 3, Java 17, Maven, JPA/Hibernate
Database: PostgreSQL 14+
DevOps: Docker, Docker Compose, Nginx
Boas práticas: Clean Code, modularização, SPA, Lazy Loading, SEO

📈 Status & Próximos Passos

Protótipo full-stack em desenvolvimento

Funcionalidades futuras: JWT, dashboard, carrinho e pagamentos, busca avançada, reviews

💡 Como Executar

Pré-requisitos: Docker Desktop, Node.js 18+, Java 17+, PostgreSQL

git clone [URL_DO_REPOSITORIO]
cd boraviajar.com.br
docker-compose up --build


Frontend: http://localhost

Backend API: http://localhost:8080

PostgreSQL: localhost:5432

🎯 Impacto

Demonstra habilidades em desenvolvimento full-stack, integração de sistemas, arquitetura modular e boas práticas de engenharia de software. Protótipo que une design moderno, UX intuitiva e backend robusto.

#FullStack #Angular #SpringBoot #Java #PostgreSQL #Docker #TravelTech #WebDevelopment #UIUX #Prototype #ResponsiveDesign
    FE -->|HTTP REST API| BE
    BE -->|JPA/Hibernate| DB
