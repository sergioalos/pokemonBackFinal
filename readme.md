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
   git clone https://github.com/sergioalos/pokemonBackFinal.git
   cd pokeapi-backend
   ```

2. **Instala dependencias:**
   ```bash
   npm install
   ```

3. **Configura las variables de entorno:**
   ```
   Esto no se deberia de subir pero por ejemplo para emular unos datos de prueba serian asi para la evaluación evitamos conflictos para la revisión a futuro se borraran

   DB_HOST=localhost

   DB_PORT=3306

   DB_NAME=pokeapi

   DB_USER=root

   DB_PASS=pokemon123

   JWT_SECRET=g2R@Z6y!uP04$XmAj1F*vm7cK2LwLQ93

4. **Levantar la bbdd:**

1º

MySQL Server	Motor de base de datos local	https://dev.mysql.com/downloads/mysql/


MySQL Workbench	GUI para trabajar con BBDD	https://dev.mysql.com/downloads/workbench/


2ºopcional pero necesario para el proyecto de back


Node.js y npm	Para correr backend Express	https://nodejs.org

3º Instalar MySQL Community Server

Elige Developer Default o Server Only.

Guarda tu contraseña de root.

Puerto por defecto: 3306.

4º Instalar workbench

Conexión BBDD

Hostname 127.0.0.1

port 3306

Conexion importante puerto 3306

username root

password obligatoria y un ejemplo 

pokemon123

5º Lo primero es decargarnos el bbddDUMP

ahora creamos la tabla pokeapi y le damos a SERVER -> DATA IMPORT ahi seleccionamos el dump y le damos a start import y se nos importará toda la BBDD

5. **Arranca el servidor en desarrollo:**
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





**Contacto:**  
Desarrollado por [Sergio].  
Email: enderman838@gmail.com


**Usuarios Aplicación**

Ejemplo de usuario root

"email": "root@pokeapi.com",

"password": "rootpassword"
