<!-- prettier-ignore-start -->

---
# 🧾 Convenciones del Proyecto – Tasku

Este documento define las **reglas de nomenclatura, estructura de código, ramas y commits** para mantener coherencia y legibilidad en todo el proyecto.

---

## 🧱 1. Estructura general

El proyecto se organiza como **monorepo modular**, con separación entre backend, frontend móvil y librerías compartidas.

```

/apps
/backend
/mobile
/libs
/shared
/docs

```

> Cada módulo debe ser **autónomo, desacoplado y reutilizable**.

---

## 🧩 2. Nomenclatura de código

| Elemento | Convención | Ejemplo |
|-----------|-------------|----------|
| **Carpetas / archivos** | `kebab-case` | `user-service.ts`, `pedidos-controller.ts` |
| **Variables y funciones** | `camelCase` | `getUserData()`, `clienteActivo` |
| **Clases y decoradores (NestJS)** | `PascalCase` | `AuthService`, `PedidosController` |
| **Constantes** | `UPPER_SNAKE_CASE` | `MAX_RETRIES = 3` |
| **Interfaces y tipos (TS)** | `PascalCase` con prefijo `I` opcional | `ICliente`, `PedidoDto` |
| **Ramas de git** | `tipo/descripcion-breve` | `feat/crear-modulo-auth`, `fix/error-login` |

---

## 🧠 3. Estilo de código

- Usar **ESLint + Prettier** en ambos entornos (backend y frontend).  
- Mantener sangría de **2 espacios**.  
- Líneas de máximo **100 caracteres**.  
- Siempre usar **comillas simples ('')** y **punto y coma al final**.  
- Nombrar las funciones con **verbos** y los componentes con **sustantivos**.  

---

## 🧱 4. Convenciones de commits

Basado en el estándar **Conventional Commits**.

### Formato

```
<tipo>(<alcance opcional>): <mensaje breve>
```

### Ejemplos

```
feat(auth): agregar validación de JWT
fix(pedidos): corregir cálculo de totales
refactor(core): reorganizar estructura de carpetas
docs(readme): actualizar documentación
style(ui): ajustar espaciado en botones
```

### Tipos válidos

| Tipo          | Uso                                       |
|---------------|-------------------------------------------|
| **feat**      | Nueva funcionalidad                       |
| **fix**       | Corrección de error                       |
| **docs**      | Cambios en documentación                  |
| **style**     | Formato o estilo visual (sin lógica)      |
| **refactor**  | Reescritura sin cambiar comportamiento    |
| **test**      | Agregado o actualización de tests         |
| **chore**     | Tareas menores o mantenimiento            |
| **perf**      | Mejoras de rendimiento                    |
| **ci**        | Cambios en pipelines o CI/CD              |

> Los mensajes deben escribirse en infinitivo y en tiempo presente.

### Reglas adicionales
- Máximo 72 caracteres en la línea principal.  
- Si el commit es grande, se puede extender con un cuerpo:

```
feat(auth): agregar validación de token JWT
* Se implementó la verificación de expiración
* Se añadió manejo de errores 401
```

---

## 🌿 5. Convenciones de ramas

| Tipo de rama  | Formato                   | Ejemplo                               |
|---------------|---------------------------|---------------------------------------|
| **Feature**   | `feat/<descripcion>`      | `feat/pantalla-login`                 |
| **Fix / Bug** | `fix/<descripcion>`       | `fix/error-login`                     |
| **Refactor**  | `refactor/<descripcion>`  | `refactorestructura-modulos`          |
| **Docs**      | `docs/<descripcion>`      | `docs/actualizar-readme`              |
| **Hotfix (urgente en prod)** | `hotfix/<descripcion>` | `hotfix/corrige-bug-jwt`  |

### Flujo sugerido
1. Crear rama desde `dev`.  
2. Commits siguiendo el formato anterior.  
3. Pull Request hacia `dev`.  
4. `main` solo recibe merges estables desde `dev`.

---

## 🧩 6. Nomenclatura en bases de datos

| Elemento          | Convención            | Ejemplo                               |
|-------------------|-----------------------|---------------------------------------|
| **Tablas**        | `snake_case` plural   | `usuarios`, `ordenes_trabajo`         |
| **Columnas**      | `snake_case`          | `fecha_creacion`, `cliente_id`        |
| **Primary Keys**  | `<tabla>_id`          | `usuario_id`, `pedido_id`             |
| **Foreign Keys**  | `fk_<tabla_origen>_<tabla_destino>` | `fk_pedidos_clientes`   |

---

## 🧰 7. Commits automáticos o dependencias
- Las actualizaciones automáticas de dependencias se etiquetan como `chore(deps): actualizar dependencias`.  
- Cambios en CI/CD: `ci(pipeline): agregar validación de tests`.

---

## 🧾 8. Referencias y convenciones recomendadas
- [Conventional Commits](https://www.conventionalcommits.org/)  
- [Commitlint](https://commitlint.js.org/#/) (para validar commits)  
- [Semantic Versioning](https://semver.org/)  
- [Git Branching Model](https://nvie.com/posts/a-successful-git-branching-model/)  

---

> 📌 Este archivo debe mantenerse actualizado si se cambia la convención o se agregan nuevas categorías de commits o ramas.

---

<!-- prettier-ignore-end -->
