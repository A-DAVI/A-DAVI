<div align="center">

# Davi Cassoli

### RPA Developer & Automation Engineer

Automating enterprise processes in accounting, fiscal, and HR domains.
From script to production-grade architecture.

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github)](https://github.com/A-DAVI)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/davi-cassoli)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail)](mailto:davicassolidev@gmail.com)

</div>

---

## Sobre mim

Desenvolvedor de automação com foco em **RPA**, **integração de IA** e **arquitetura de sistemas backend**.

Trabalho na [@GRUPO14D](https://grupo14d.com.br) como desenvolvedor responsável por toda a infraestrutura de automações: 15 RPAs em produção cobrindo processos fiscais, contábeis, financeiros e de RH. Construí do zero o **MONITOR-RPA**, dashboard full-stack para monitoramento em tempo real de todos os robôs, o **grupo14d-toolkit**, monorepo Python que sustenta o ecossistema, e o **NFS-e Forms**, plataforma SaaS interna que automatiza a emissão de notas fiscais via portal Elotech, hoje em produção.

Atualmente cursando **Análise e Desenvolvimento de Sistemas** na UniCesumar (5º semestre) e aprofundando em engenharia de IA: LLMs, RAG, MCP e agentes em produção.

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
![Neon](https://img.shields.io/badge/Neon-00E599?style=for-the-badge&logo=postgresql&logoColor=white)
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
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

---

## Projetos em destaque

### [MONITOR-RPA](https://github.com/GRUPO14D/MONITOR-RPA) · v2.4.1

Dashboard full-stack de observabilidade para os 15 RPAs em produção no Grupo 14D.

- SSE com fallback para polling no streaming de eventos em tempo real
- Fila de jobs in-memory (substituiu o `pg_boss`), reconstruída a partir do estado a cada boot
- Views dedicadas: live, operations, monthly, business, agents, observers e config
- Integra `grupo14d-telemetry` com heartbeat e telemetria de CPU/memória via `psutil`
- Alertas por email em construção (watchdog de heartbeat, erro de RPA e job falho)
- Deploy via Vercel (web) + pm2 (API desacoplada de sessão RDP)

**Stack:** TypeScript · React · Vite · Fastify · PostgreSQL (Neon) · pm2

---

### NFS-e Forms · em produção

Plataforma SaaS interna que automatiza a emissão de notas fiscais de serviço no portal Elotech (OXY) para os clientes do Grupo 14D.

- Frontend React/Vite no Vercel onde o cliente preenche e envia a solicitação
- Backend serverless enfileira o job no Neon/PostgreSQL via `pg_boss`
- Worker interno em Python consome a fila e dispara a automação via framework `grupo14d-observer`
- Captura o PDF da nota por route intercept, extrai o número da NFS-e e envia por email ao tomador e ao time interno
- Do formulário ao PDF no email do cliente em 3 a 5 minutos, sem intervenção manual
- Telemetria por job integrada ao MONITOR-RPA

**Stack:** Python · Playwright · React · Vite · Node.js · PostgreSQL · pg_boss

---

### grupo14d-toolkit

Monorepo Python que é a espinha dorsal técnica do ecossistema de automação do Grupo 14D. Pacotes distribuídos via pip + PAT.

- **`grupo14d-telemetry`** `v0.1.0` · estável: reporte de eventos e heartbeats via thread daemon, `TelemetryConfig` em cascata de 3 camadas e compatibilidade com PyInstaller. Integrado nos 15 RPAs, 77 testes verdes.
- **`grupo14d-ml`** · dev: inferência local com LinearSVC + TF-IDF para classificação de contas de cartórios. Em produção no RPA-Cartórios.
- **`grupo14d-observer`** · dev: aprendizado por observação. Grava sessões Playwright e gera harnesses de navegação automaticamente. `ElotechExplorer` com BFS, `SemanticMatcher` e auto-labeler.
- **`grupo14d-bot`** · dev: notificações por email via Gmail API. Qualquer RPA dispara alertas tipados (`error` / `alert` / `info`) com uma linha. OAuth2, config em cascata e templates HTML por severidade.

**Stack:** Python · Playwright · scikit-learn · Gmail API · Pytest · PyInstaller

---

### RPA-IRPF

Ecossistema de automação para processamento de declarações de IRPF em ambiente contábil.

- RPA-016: watcher com polling via SMB, detecção e renomeação automática de arquivos via watchdog
- RPA-017: sync guardian com reconciliação Google Sheets, lógica de `PENDING_MATCH` retry e deduplicação por CPF
- Todos em produção sob pm2 com heartbeat e telemetria integrada ao MONITOR-RPA

**Stack:** Python · Google Sheets API · pm2 · Watchdog

---

### [MyBuddy](https://github.com/EderHenriq/MyBuddy)

Plataforma que centraliza adoção, serviços, eventos e marketplace pet, conectando adotantes, ONGs, pet shops e clínicas veterinárias.

- Autenticação federada com **Keycloak 26** + OAuth2/PKCE e `KeycloakUserSyncService` com fallback por email
- Gateway de pagamento **Mercado Pago** com Checkout Pro, webhook validado via HMAC-SHA256, listener assíncrono com Spring Events + `@Async`, polling de status e telas de confirmação/pendente
- Angular 21 com signals, lazy loading e Payment Brick integrado como segunda opção de checkout
- Infraestrutura Docker com PostgreSQL, MongoDB, Keycloak e ngrok para testes de webhook local

**Stack:** Java 21 · Spring Boot 3.5 · Angular 21 · Flutter · Keycloak 26 · Mercado Pago · Docker · MongoDB · PostgreSQL

> Projeto acadêmico (TCC) · Time de 4 devs · UniCesumar 2026

---

## Foco atual

- Liberando o **NFS-e Forms** para os clientes do Grupo 14D após o primeiro ciclo completo em produção
- Construindo o **`grupo14d-bot`**, quarto pacote do toolkit, para centralizar notificações por email de todos os RPAs
- Finalizando o TCC **MyBuddy**: integração Mercado Pago (Checkout Pro + webhook) e Flutter conectado ao backend Spring Boot com Keycloak
- Aprofundando em **engenharia de IA**: RAG, MCP, agentes e inferência local (Ollama)
- Construindo base sólida em **algoritmos, estruturas de dados e system design**

---

<div align="center">
<sub>Maringá, PR · davicassolidev@gmail.com</sub>
</div>
