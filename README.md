# 🧭 Proyecto: Tasku

**Tasku** es una aplicación móvil para la **contratación de servicios de mantenimiento del hogar** y la **compra de materiales e insumos** relacionados.  
El ecosistema integra servicios, tienda, chat y videoasistencia en una sola plataforma.

---

## 🚀 Objetivo

Desarrollar un **proyecto completo y escalable** que sirva como demostración técnica de:

- buenas prácticas de desarrollo full stack,
- arquitectura limpia (Clean / Hexagonal),
- y uso combinado de tecnologías modernas (SQL + NoSQL, tiempo real, autenticación, pagos).

> 📄 Más detalles en [`VISION.md`](./VISION.md)

---

## 👥 Roles de usuario

- **Administradores** → gestión global del sistema
- **Vendedores** → gestión de productos y pedidos
- **Proveedores** → abastecimiento y control de entregas
- _(Futuros: Clientes / Trabajadores para servicios)_

---

## 🧩 Módulos principales

- **Auth / Usuarios**
- **Servicios** (solicitud y agendamiento)
- **Tienda (Store)**
- **Chat / Soporte**
- **Pagos y Suscripciones**
- **Notificaciones**

> 📄 Ver más en [`docs/ideas.md`](./docs/ideas.md)

---

## 🛠️ Tecnologías base

| Categoría           | Herramientas                             |
| ------------------- | ---------------------------------------- |
| **Backend**         | NestJS (TypeScript)                      |
| **Frontend móvil**  | React Native (Expo)                      |
| **DB**              | PostgreSQL (Prisma) + MongoDB (Mongoose) |
| **Autenticación**   | JWT / Firebase Auth                      |
| **Chat**            | Socket.io + MongoDB                      |
| **Videochat**       | WebRTC / Twilio / Jitsi                  |
| **Infraestructura** | Docker + Railway / Render                |

---

## 🧱 Arquitectura

- **Monorepo modular (Nx / TurboRepo)**
- **Backend con Clean Architecture / Hexagonal Design**
- **API Gateway central**
- **Módulos desacoplados:** `auth`, `users`, `services`, `store`, `chat`
- Preparado para escalar a **microservicios independientes**

> 📄 Diagrama y diseño técnico en [`docs/architecture.md`](./docs/architecture.md)

---

## 📅 Estado actual

📍 **Etapa de planificación y diseño (pre-codeo)**  
Definición de módulos, arquitectura y stack inicial.  
Siguiente paso: diseño técnico del backend y estructura de monorepo.

> 📄 Roadmap completo en [`ROADMAP.md`](./ROADMAP.md)
