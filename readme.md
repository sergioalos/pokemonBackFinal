# PokéAPI - Backend

PokéAPI es una API RESTful para gestionar equipos, Pokémon, combates y estadísticas en un entorno competitivo inspirado en el universo Pokémon. Este backend está desarrollado con Node.js, Express y Sequelize sobre MySQL.

---

## 🚀 Características Principales

- 🔐 **Autenticación JWT:** Registro y login de usuarios.
- 👥 **Gestión de equipos:** Crear, editar, eliminar y consultar equipos de 4 Pokémon.
- 🐱‍👓 **Gestión de Pokémon:** CRUD completo para administradores.
- 🌈 **Asignación de tipos:** Relaciona Pokémon con sus tipos.
- ⚔️ **Sistema de combates:** Inicia combates entre equipos, registra rondas y determina ganadores.
- 📊 **Historial y estadísticas:** Consulta historial de combates y ranking global.
- 🛡️ **Panel de administración:** Gestión avanzada de usuarios, equipos y combates (solo root).
- 🧪 **Cobertura de tests:** Tests automáticos con Jest y Supertest.

---

## 🛠️ Tecnologías Utilizadas

| Nombre         | Descripción                |
| -------------- | ------------------------- |
| Node.js        | Backend JavaScript        |
| Express        | Framework API RESTful     |
| Sequelize      | ORM para MySQL            |
| MySQL          | Base de datos relacional  |
| JWT            | Autenticación segura      |
| Jest & Supertest | Testing automático      |

---

## ⚡ Instalación Rápida

```bash
git clone https://github.com/sergioalos/pokemonBackFinal.git
cd pokemonBackFinal
npm install
```

---

### 1️⃣ Configuración de variables de entorno

Crea un archivo `.env` en la raíz con estos valores de ejemplo:

```properties
DB_HOST=localhost
DB_PORT=3306
DB_NAME=pokeapi
DB_USER=root
DB_PASS=pokemon123
JWT_SECRET=g2R@Z6y!uP04$XmAj1F*vm7cK2LwLQ93
```

---

### 2️⃣ Base de datos MySQL

- Instala MySQL Server y Workbench.
- Crea la base de datos `pokeapi`.
- Importa el dump desde: **SERVER → DATA IMPORT**.
- Puerto por defecto: `3306`.
- Usuario: `root`.
- Contraseña de ejemplo: `pokemon123`.

---

### 3️⃣ Arranca el servidor

```bash
npm run dev
```

---

## 📚 Endpoints Principales

<details>
  <summary><b>Autenticación</b></summary>

  - `POST /auth/register` — Registro de usuario
  - `POST /auth/login` — Login y obtención de token JWT
</details>

<details>
  <summary><b>Equipos</b></summary>

  - `POST /teams` — Crear equipo
  - `GET /teams/my` — Ver equipos propios
  - `PUT /teams/:id` — Editar equipo
  - `DELETE /teams/:id` — Eliminar equipo
</details>

<details>
  <summary><b>Pokémon</b></summary>

  - `GET /pokemons` — Listar Pokémon
  - `POST /pokemons` — Crear Pokémon (root)
  - `PUT /pokemons/:id` — Editar Pokémon (root)
  - `DELETE /pokemons/:id` — Eliminar Pokémon (root)
</details>

<details>
  <summary><b>Tipos y efectividad</b></summary>

  - `GET /types` — Listar tipos
  - `POST /effectiveness` — Crear relación de efectividad (root)
</details>

<details>
  <summary><b>Combates</b></summary>

  - `POST /battles` — Iniciar combate
  - `POST /battles/:id/rounds` — Iniciar ronda
  - `GET /battles/my-history` — Ver historial de combates
</details>

<details>
  <summary><b>Estadísticas</b></summary>

  - `GET /stats/ranking` — Ranking global
  - `GET /stats/my-stats` — Estadísticas propias
</details>

<details>
  <summary><b>Administración (solo root)</b></summary>

  - `GET /admin/users` — Listar usuarios
  - `DELETE /admin/users/:id` — Eliminar usuario
  - `GET /admin/teams` — Listar todos los equipos
  - `GET /admin/battles` — Listar todos los combates
</details>

---

## 🧪 Testing

Ejecuta los tests automáticos con cobertura:

```bash
npm test
```

---

## 🗂️ Estructura del Proyecto

```
src/
 ├── app.js
 ├── routes/
 ├── models/
 ├── middleware/
 ├── utils/
 ├── config/
 └── ...
```

---

## 👤 Contacto

Desarrollado por: **Sergio**  
📧 Email: enderman838@gmail.com

---

## 🗝️ Usuarios de ejemplo

```json
{
  "email": "root@pokeapi.com",
  "password": "rootpassword"
}
```

---
