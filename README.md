<div align="center">

# Davi Cassoli

### RPA Developer & Automation Engineer

Automating enterprise processes in accounting, fiscal, and HR domains —
from script to production-grade architecture.

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github)](https://github.com/A-DAVI)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/davi-cassoli)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail)](mailto:davicassolidev@gmail.com)

</div>

---

## Sobre mim

Desenvolvedor de automação com foco em **RPA**, **integração de IA** e **arquitetura de sistemas backend**.

Trabalho na [@GRUPO14D](https://grupo14d.com.br) como desenvolvedor responsável por toda a infraestrutura de automações — 15 RPAs em produção cobrindo processos fiscais, contábeis, financeiros e de RH. Construí do zero o **MONITOR-RPA**, um dashboard full-stack para monitoramento em tempo real de todos os robôs, e o **NFS-e Forms**, uma plataforma SaaS interna que automatiza a emissão de notas fiscais via portal Elotech com fila de jobs e telemetria integrada.

Atualmente cursando **Análise e Desenvolvimento de Sistemas** na UniCesumar (5º semestre) e aprofundando em engenharia de IA — LLMs, RAG, MCP e agentes em produção.

---

## Stack

### Backend
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Java 21](https://img.shields.io/badge/Java%2021-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot 3](https://img.shields.io/badge/Spring%20Boot%203-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Fastify](https://img.shields.io/badge/Fastify-000000?style=for-the-badge&logo=fastify&logoColor=white)

### Frontend & Mobile
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)

### Banco de Dados
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)

### DevOps & Ferramentas
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![pm2](https://img.shields.io/badge/pm2-2B037A?style=for-the-badge&logo=pm2&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

### IA & Automação
![Claude AI](https://img.shields.io/badge/Claude%20AI-FF6B6B?style=for-the-badge&logo=anthropic&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)

---

## Projetos em destaque

### [MONITOR-RPA](https://github.com/GRUPO14D/MONITOR-RPA)

Dashboard full-stack para monitoramento em tempo real de 15 RPAs em produção no Grupo 14D.

- SSE para streaming de eventos em tempo real
- Biblioteca `grupo14d-telemetry` (PyPI-style, pip+PAT) com `HeartbeatDaemon`, `TelemetryConfig` em cascata de 3 camadas e compatibilidade com PyInstaller — 77 testes, 100% verdes
- Fila de jobs via `pg_boss` integrada ao Neon/PostgreSQL
- Deploy contínuo via Vercel + pm2 desacoplado de sessão RDP

**Stack:** TypeScript · React · Vite · Fastify · PostgreSQL (Neon) · pm2

---

### NFS-e Forms

Plataforma SaaS interna que automatiza a emissão de notas fiscais de serviço no portal Elotech (OXY) para os clientes do Grupo 14D.

- Frontend React/Vite (Vercel) + backend Node.js serverless que enfileira jobs via `pg_boss`
- Worker interno em Fastify consome a fila e dispara automação via framework `grupo14d-observer`
- `grupo14d-observer` gera harnesses de navegação automaticamente via análise de DOM — novos portais exigem mínima configuração manual
- Telemetria integrada ao MONITOR-RPA com eventos de ciclo de vida por job

**Stack:** Python · Playwright · React · Vite · Node.js · Fastify · PostgreSQL · pg_boss

---

### grupo14d-toolkit

Espinha dorsal técnica do ecossistema de RPAs do Grupo 14D.

- `grupo14d-telemetry`: reporte de eventos e heartbeats via thread daemon, distribuído via PAT
- `grupo14d-observer`: framework de automação com geração automática de harnesses de navegação
- Audit Engine: auditoria estática dos 15 RPAs (~47k LOC) com roadmap de saneamento
- 77 testes unitários · 100% verdes

**Stack:** Python · FastAPI · Pytest · PyInstaller

---

### RPA-IRPF

Ecossistema de automação para processamento de declarações de IRPF em ambiente contábil.

- RPA-016: watcher com polling via SMB, detecção e renomeação automática de arquivos via watchdog
- RPA-017: sync guardian com reconciliação Google Sheets, lógica de `PENDING_MATCH` retry e deduplicação por CPF
- Todos em produção sob pm2 com heartbeat e telemetria integrada

**Stack:** Python · Google Sheets API · pm2 · Watchdog

---

### [MyBuddy](https://github.com/EderHenriq/MyBuddy)

Plataforma que centraliza adoção, serviços, eventos e marketplace pet — conectando adotantes, ONGs, pet shops e clínicas veterinárias.

- Autenticação federada com **Keycloak 26** + OAuth2/PKCE e `KeycloakUserSyncService` com fallback por email
- Gateway de pagamento **Mercado Pago** com Checkout Pro, webhook validado via HMAC-SHA256, listener assíncrono com Spring Events + `@Async`, polling de status e telas de confirmação/pendente
- Angular 21 com signals, lazy loading e Payment Brick integrado como segunda opção de checkout
- Infraestrutura Docker com PostgreSQL, MongoDB, Keycloak e ngrok para testes de webhook local

**Stack:** Java 21 · Spring Boot 3.5 · Angular 21 · Flutter · Keycloak 26 · Mercado Pago · Docker · MongoDB · PostgreSQL

> Projeto acadêmico (TCC) · Time de 4 devs · UniCesumar 2026

---

## Foco atual

- Finalizando o TCC **MyBuddy** — integrando Flutter ao backend Spring Boot com autenticação Keycloak
- Expandindo o ecossistema de RPAs no Grupo 14D com integração de **LLMs como micro-agentes** dentro de cada RPA
- Aprofundando em **engenharia de IA**: RAG, MCP, agentes e inferência local (Ollama)
- Construindo base sólida em **algoritmos, estruturas de dados e system design**

---

<div align="center">
<sub>Maringá, PR · davicassolidev@gmail.com</sub>
</div>
