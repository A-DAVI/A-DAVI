<div align="center">

# Davi Cassoli

### Software Engineer · Data & Automation

Building data-driven platforms for accounting and fiscal domains.
From document parsing to production systems with real business impact.

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github)](https://github.com/A-DAVI)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/davi-cassoli)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail)](mailto:davicassolidev@gmail.com)

</div>

---

## Sobre mim

Engenheiro de software com foco em **plataformas de dados**, **automação de processos fiscais** e **arquitetura backend**.

Na [@GRUPO14D](https://grupo14d.com.br) sou responsável por toda a infraestrutura tecnológica: projetei e implementei o **SIMTRIB** (plataforma de análise tributária com parser de documentos fiscais, ORM, API e frontend), o **MONITOR-RPA** (dashboard de observabilidade em tempo real), o **grupo14d-toolkit** (monorepo que sustenta o ecossistema) e mais de 15 automações em produção cobrindo processos fiscais, contábeis e de RH.

Cursando **Análise e Desenvolvimento de Sistemas** na UniCesumar (5º semestre). Caminhando para engenharia de IA e dados.

---

## Stack principal

### Backend & Data
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=for-the-badge&logo=sqlalchemy&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

### Frontend
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)

### Infra
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-FF9900?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)

---

## Projetos

### [SIMTRIB](https://github.com/GRUPO14D/SIMTRIB) · em produção

Plataforma de análise tributária que automatiza o estudo fiscal de novos clientes, substituindo processo manual que travava o sistema Domínio por horas.

- Parser de NF-e, PGDAS e e-Social com 9 relatórios analíticos validados contra o Domínio
- ORM com 17 models, upsert idempotente, soft delete e Alembic migrations
- API FastAPI com routers por módulo, base Siscomex de NCMs integrada
- Frontend React 19 com Radix UI e design system Impeccable
- Deploy via Docker Compose (PostgreSQL + backend + frontend + nginx)
- CI com GitHub Actions (pytest + Postgres, ruff, oxlint, tsc), governança com AGENTS.md versionado

**Stack:** Python · FastAPI · SQLAlchemy 2.0 · PostgreSQL · React 19 · Docker · GitHub Actions

---

### [MONITOR-RPA](https://github.com/GRUPO14D/MONITOR-RPA) · v2.4.1

Dashboard de observabilidade em tempo real para 15+ automações em produção.

- SSE com fallback para polling, fila de jobs in-memory reconstruída a cada boot
- 7 views: live, operations, monthly, business, agents, observers e config
- Integra grupo14d-telemetry com heartbeat e telemetria de CPU/memória

**Stack:** TypeScript · React · Fastify · PostgreSQL (Neon) · pm2

---

### grupo14d-toolkit

Monorepo Python que sustenta o ecossistema de automação. Pacotes distribuídos via pip + PAT.

- **telemetry** `v0.1.0` — eventos e heartbeats via thread daemon, config em cascata, 77 testes. Integrado nos 15 RPAs
- **ml** — classificação de contas com LinearSVC + TF-IDF. Em produção no RPA-Cartórios
- **observer** — aprendizado por observação com Playwright. BFS em portais, auto-labeler
- **bot** — notificações por email via Gmail API com templates por severidade

---

### [MyBuddy](https://github.com/EderHenriq/MyBuddy) · TCC

Plataforma pet (adoção, serviços, marketplace) deployada na AWS com 7 containers.

- Java 21 + Spring Boot 3.5, Angular 21, Flutter com Clean Architecture
- Keycloak 26 + OAuth2/PKCE, Mercado Pago com webhook HMAC-SHA256
- AWS EC2 com Caddy, Docker Compose e volumes persistentes

> Projeto acadêmico · Time de 4 devs · UniCesumar 2026

---

## Foco atual

- **SIMTRIB** — capitulação de NCMs (Fase 2), consulta de tributação por produto/segmento
- **Ecossistema Grupo 14D** — padronização de telemetria e build across 22 RPAs
- **Engenharia de IA** — agentes, RAG e integração de LLMs em domínio fiscal
- **System design** — arquitetura de dados, pipelines ETL, integração de APIs públicas (Siscomex, BrasilAPI, Calculadora CBS)

---

<div align="center">
<sub>Jandaia do Sul, PR · davicassolidev@gmail.com</sub>
</div>
