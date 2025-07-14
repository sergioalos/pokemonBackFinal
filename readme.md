# PokéAPI - Backend

PokéAPI es una API RESTful para gestionar equipos, Pokémon, combates y estadísticas en un entorno competitivo inspirado en el universo Pokémon. Este backend está desarrollado con Node.js, Express y Sequelize sobre MySQL.

## Características principales

- **Autenticación JWT:** Registro y login de usuarios.
- **Gestión de equipos:** Crear, editar, eliminar y consultar equipos de 4 Pokémon.
- **Gestión de Pokémon:** CRUD completo para administradores.
- **Asignación de tipos:** Relaciona Pokémon con sus tipos.
- **Sistema de combates:** Inicia combates entre equipos, registra rondas y determina ganadores.
- **Historial y estadísticas:** Consulta historial de combates y ranking global.
- **Panel de administración:** Gestión avanzada de usuarios, equipos y combates (solo root).
- **Cobertura de tests:** Tests automáticos con Jest y Supertest.

## Tecnologías

- Node.js
- Express
- Sequelize (ORM)
- MySQL
- JWT (autenticación)
- Jest & Supertest (testing)

## Instalación

1. **Clona el repositorio:**
   ```bash
   git clone https://github.com/tuusuario/pokeapi-backend.git
   cd pokeapi-backend
   ```

2. **Instala dependencias:**
   ```bash
   npm install
   ```

3. **Configura las variables de entorno:**
   Crea un archivo `.env` en la raíz con el siguiente contenido:
   ```
   DB_NAME=tu_base_de_datos
   DB_USER=tu_usuario
   DB_PASS=tu_contraseña
   DB_HOST=localhost
   DB_PORT=3306
   JWT_SECRET=tu_secreto_jwt
   ```

4. **Arranca el servidor en desarrollo:**
   ```bash
   npm run dev
   ```

## Endpoints principales

### Autenticación

- `POST /auth/register` — Registro de usuario
- `POST /auth/login` — Login y obtención de token JWT

### Equipos

- `POST /teams` — Crear equipo
- `GET /teams/my` — Ver equipos propios
- `PUT /teams/:id` — Editar equipo
- `DELETE /teams/:id` — Eliminar equipo

### Pokémon

- `GET /pokemons` — Listar Pokémon
- `POST /pokemons` — Crear Pokémon (root)
- `PUT /pokemons/:id` — Editar Pokémon (root)
- `DELETE /pokemons/:id` — Eliminar Pokémon (root)

### Tipos y efectividad

- `GET /types` — Listar tipos
- `POST /effectiveness` — Crear relación de efectividad (root)

### Combates

- `POST /battles` — Iniciar combate
- `POST /battles/:id/rounds` — Iniciar ronda
- `GET /battles/my-history` — Ver historial de combates

### Estadísticas

- `GET /stats/ranking` — Ranking global
- `GET /stats/my-stats` — Estadísticas propias

### Administración (solo root)

- `GET /admin/users` — Listar usuarios
- `DELETE /admin/users/:id` — Eliminar usuario
- `GET /admin/teams` — Listar todos los equipos
- `GET /admin/battles` — Listar todos los combates

## Testing

Ejecuta los tests con cobertura:
```bash
npm test
```

## Estructura del proyecto

```
src/
  app.js
  routes/
  models/
  middleware/
  utils/
  config/
  ...
```

## Contribución

Las contribuciones son bienvenidas. Por favor, abre un issue o pull request para sugerencias o mejoras.

## Licencia

Este proyecto está bajo la licencia ISC.

---

**Contacto:**  
Desarrollado por [Sergio].  
Email: enderman838@gmail.com


Usuarios ej
"email": "root@pokeapi.com",
"password": "rootpassword"
