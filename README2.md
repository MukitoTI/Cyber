# 🚀 Secure SaaS Dashboard (Spring Boot + React + Docker)

## 📌 Visão Geral

Este projeto é um **SaaS com Dashboard seguro**, desenvolvido com foco em:

- Arquitetura moderna (Full Stack)
- Segurança baseada no OWASP Top 10
- Execução local com Docker
- Pronto para evolução para produção

---

## 🎯 Funcionalidades

- 🔐 Autenticação segura (JWT + Refresh Token)
- 👥 Controle de usuários (RBAC: Admin / User)
- 📊 Dashboard com dados simulados
- 🧾 Logs e auditoria de acesso
- 🛡️ Proteção contra ataques comuns (SQL Injection, XSS, CSRF, etc.)

---

## 🏗️ Arquitetura

### Backend

- Java 17+
- Spring Boot
- Spring Security
- JPA (Hibernate)

### Frontend

- React
- Vite
- Axios

### Banco de Dados

- PostgreSQL

### Infraestrutura

- Docker
- Docker Compose

---

## 🔐 Segurança Implementada

- Hash de senha com bcrypt
- JWT com expiração + refresh token
- Proteção contra SQL Injection (ORM + queries parametrizadas)
- Proteção contra XSS (sanitização + escape)
- Proteção contra CSRF
- Headers de segurança
- Rate limiting (anti brute force)
- RBAC (controle de acesso por perfil)
- Logs de autenticação

---

## 🧰 Pré-requisitos (INSTALAR ANTES)

Antes de rodar o projeto, instale:

### 🔧 Essenciais

- [ ] **Java JDK 17 ou superior**
- [ ] **Node.js (versão LTS)**
- [ ] **Docker**
- [ ] **Docker Compose**
- [ ] **Git**

---

### 🧪 Recomendado (Dev)

- [ ] VS Code ou IntelliJ IDEA
- [ ] Postman ou Insomnia
- [ ] DBeaver (ou outro client PostgreSQL)

---

## 📦 Instalação das Ferramentas

### Java

```bash
java -version

```
### Node.js

node -v
npm -v
```

### Docker
docker -v
docker-compose -v
