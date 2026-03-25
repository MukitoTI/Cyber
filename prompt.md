# 🚀 PROMPT PROFISSIONAL – SAAS SEGURO (FULL STACK)

## 🧠 CONTEXTO

Atue como um arquiteto de software sênior, especialista em segurança de aplicações web (OWASP Top 10), engenharia de backend, DevSecOps e SaaS escalável.

O objetivo é projetar e desenvolver um SaaS completo com dashboard administrativo, com foco extremo em segurança, boas práticas e arquitetura moderna.

O sistema deve rodar LOCALMENTE (ambiente de desenvolvimento), mas com arquitetura pronta para produção.

---

## 🎯 OBJETIVO DO SAAS

Criar um sistema SaaS com:

- Login seguro  
- Dashboard administrativo  
- Controle de usuários (RBAC)  
- API segura  
- Banco de dados protegido  

---

## 🏗️ ARQUITETURA

Definir e implementar:

- **Backend:** Java (Spring Boot) ou Node.js (NestJS)  
- **Frontend:** React (Vite ou Next.js)  
- **Banco de dados:** PostgreSQL  
- **Autenticação:** JWT + Refresh Token  
- **Containerização:** Docker  
- **Arquitetura:** Camadas (Controller, Service, Repository)  

---

## 🔐 SEGURANÇA (OBRIGATÓRIO)

Implementar e explicar:

### 1. SQL Injection
- Uso de ORM (Hibernate / Prisma)  
- Queries parametrizadas  

### 2. XSS (Cross-Site Scripting)
- Sanitização de entrada  
- Escape de saída no frontend  

### 3. CSRF
- Tokens CSRF  
- Cookies com SameSite  

### 4. Autenticação
- Hash de senha com bcrypt  
- Política de senha forte  
- Refresh tokens seguros  
- Expiração de sessão  

### 5. Autorização
- RBAC (Admin, User)  
- Middleware de autorização  

### 6. Headers de Segurança
- Content-Security-Policy  
- X-Frame-Options  
- X-XSS-Protection  

### 7. Rate Limiting
- Proteção contra brute force  

### 8. Logs e Auditoria
- Log de login  
- Tentativas inválidas  

---

## 🧪 TESTES DE SEGURANÇA

Simular e proteger contra:

- SQL Injection (`' OR 1=1 --`)  
- XSS (`<script>alert(1)</script>`)  
- Ataques de força bruta  

Criar exemplos de testes automatizados ou scripts de validação.

---

## 🖥️ FUNCIONALIDADES DO DASHBOARD

- Tela de login  
- Cadastro de usuário  
- Dashboard com dados simulados  
- Perfil do usuário  
- Controle de permissões  

---

## 🐳 EXECUÇÃO LOCAL

Explicar passo a passo:

1. Instalar dependências  
2. Configurar variáveis de ambiente (`.env`)  
3. Rodar com Docker Compose  
4. Acessar no navegador  

---

## 📁 ESTRUTURA DO PROJETO

Apresentar:

- Estrutura de pastas  
- Arquivos principais  
- Código inicial funcional  

---

## 🔥 EXTRA (DIFERENCIAL)

- Implementar 2FA (opcional)  
- Proteção contra CORS mal configurado  
- Validação com Zod ou class-validator  
- Boas práticas de API REST  

---

## 📌 IMPORTANTE

- Código deve ser funcional  
- Seguir boas práticas reais de mercado  
- Explicar cada decisão de segurança  
- Pensar como sistema pronto para produção  

---

## ✅ SAÍDA ESPERADA

Gerar:

1. Arquitetura completa  
2. Código base  
3. Passo a passo de execução  
4. Explicação das proteções implementadas  

---

## 💡 DICA DE USO

Após gerar o resultado, evoluir iterativamente:

- "Vamos começar pelo backend"
- "Agora implemente autenticação"
- "Agora testar vulnerabilidades"

---

## ⚠️ ALERTAS

Evitar:

- Supor segurança absoluta (não existe sistema 100% inviolável)  
- Não validar entradas  
- Confiar apenas no frontend  
- Não implementar controle de sessão adequado  

---

## 🚀 EVOLUÇÕES FUTURAS

- SaaS multi-tenant  
- Deploy em cloud (AWS, Azure)  
- CI/CD seguro  
- Pentest ético estruturado  
