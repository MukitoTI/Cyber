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
```bash
node -v
npm -v
```

### Docker
```
docker -v
docker-compose -v
```

----------------------------------------------------------------

# 📁 Estrutura do Projeto

```
secure-saas/
│
├── backend/
│   ├── src/
│   ├── pom.xml
│
├── frontend/
│   ├── src/
│   ├── package.json
│
├── docker/
│   ├── docker-compose.yml
│
├── .env
└── README.md


```

------------------------------------------------------------


# ⚙️ Configuração do Ambiente

Crie um arquivo `.env` na raiz:
```
# Backend
SPRING_DATASOURCE_URL=jdbc:postgresql://db:5432/saas_db
SPRING_DATASOURCE_USERNAME=postgres
SPRING_DATASOURCE_PASSWORD=postgres

JWT_SECRET=super_secret_key
JWT_EXPIRATION=3600000

# Frontend
VITE_API_URL=http://localhost:8080
```

--------------------------------------------------------------

# 🐳 Executando o Projeto
## 1. Subir os containers
```Bash
docker-compose up --build

```

-------------------------------------------------------------

## 2. Acessar o sistema
  * Frontend: http://localhost:5173
  * Backend: http://localhost:8080

------------------------------------------------------------

## 🔐 Fluxo de Autenticação
  1. Usuário faz login
  2. Backend valida credenciais
  3. Retorna:
      * Access Token (curto prazo)
      * Refresh Token (longo prazo)
  4. Frontend usa token nas requisições

------------------------------------------------------------

### 🧪 Testes de Segurança
SQL Injection

Testar input:

```
' OR 1=1 --
```
✔️ Deve ser bloqueado pelo ORM

--------------------------------------------------------------
### XSS

Testar input:
```
<script>alert('xss')</script>
```
✔️ Deve ser sanitizado

--------------------------------------------------------------

### Brute Force
  * Simular múltiplos logins
  * Sistema deve aplicar rate limiting

--------------------------------------------------------------

### 📊 RBAC (Controle de Acesso)

Perfis:

  * **ADMIN**
    * Acesso total
  * **USER**
    * Acesso limitado

-----------------------------------------------------------

### 🛡️ Boas Práticas Aplicadas
  * Separação de camadas (Controller, Service, Repository)
  * Validação de entrada
  * Uso de variáveis de ambiente
  * Não expor dados sensíveis
  * Logs estruturados

-----------------------------------------------------------

### 🚀 Roadmap (Próximos Passos)
  * [] Implementar 2FA
  * [] Multi-tenant (vários clientes)
  * [] Deploy em cloud (AWS/Azure)
  * [] CI/CD pipeline
  * [] Monitoramento (Prometheus + Grafana)

------------------------------------------------------------

### ⚠️ Avisos Importantes
  * Não existe sistema 100% seguro
  * Segurança é um processo contínuo
  * Sempre atualizar dependências

----------------------------------------------------------

### 👨‍💻 Próxima Etapa

➡️ Gerar o código base:
  * Backend (Spring Boot)
  * Frontend (React)
  * Docker Compose


```

---

Se quiser, próximo passo já vamos direto pro **código real (backend Spring Boot)** — e aí começa a parte mais interessante 🔥
```
