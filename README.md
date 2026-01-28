# 🎫 Ticket SLA API

API REST para gerenciamento de tickets com regras de SLA (prazo por prioridade), status e auditoria de alterações.  
Projeto focado em boas práticas de arquitetura, organização de código e regras de negócio.

---

## ✅ Features
- CRUD de tickets
- SLA automático por prioridade (LOW / MED / HIGH / URGENT)
- Cálculo de `dueAt` e status do SLA:
  - `ON_TIME`
  - `AT_RISK` (quando restam ≤ 20% do tempo do SLA)
  - `BREACHED`
- Auditoria de mudanças (status, responsável e prioridade)
- Filtros por status, prioridade, categoria e responsável

---

## 🧰 Stack
- Node.js
- TypeScript
- Express
- PostgreSQL
- Prisma ORM
- Docker
- Swagger (OpenAPI)

---

## 🗂️ Estrutura do Projeto
```bash
ticket-sla-api/
  src/
    config/
    modules/
      tickets/
      users/
      audit/
    shared/
      errors/
      middlewares/
      utils/
        sla.ts
    app.ts
    server.ts
  prisma/
  docker-compose.yml
  .env.example
  README.md
