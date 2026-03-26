# Enfokids

Orquestador Docker para levantar la aplicación completa de Enfokids.

Incluye tres servicios:
- **enfokids-api** — Backend Spring Boot (Java 21) en `localhost:8080`
- **enfokids-client** — Frontend Astro + Bun en `localhost:4321`
- **db** — PostgreSQL 16

---

## Requisitos previos

- [Docker Desktop](https://www.youtube.com/watch?v=IMqYPAwX3iM) instalado y corriendo
- [Git](https://git-scm.com/) instalado

---

## Estructura esperada

Antes de continuar, esta carpeta debe tener la siguiente estructura:

```
enfokids/
├── docker-compose.yml
├── .env.example
├── .env                ← creado a partir de .env.example (no se sube al repo)
├── enfokids-api/       ← repositorio del backend
└── enfokids-client/    ← repositorio del frontend
```

---

## Paso 1 — Clonar los proyectos

Dentro de esta carpeta (`enfokids/`), clona ambos repositorios:

```bash
git clone https://github.com/cawtoz/enfokids-api.git
git clone https://github.com/cawtoz/enfokids-client.git
```

> Si ya tienes los proyectos clonados, asegúrate de que estén nombrados exactamente `enfokids-api` y `enfokids-client`.

---

## Paso 2 — Configurar las variables de entorno

Copia el archivo de ejemplo y completa los valores:

```bash
cp .env.example .env
```

Edita el archivo `.env` con tus propios valores:

```env
# Base de datos
DATABASE_NAME=enfokids
DATABASE_USERNAME=postgres
DATABASE_PASSWORD=your_password_here

# Hibernate (usa "create" la primera vez, luego cambia a "update")
HIBERNATE_DDL_AUTO=update

# JWT
JWT_SECRET_KEY=your_super_secret_key_at_least_256_bits_long
JWT_EXPIRATION_TIME=3600000
```

---

## Paso 3 — Levantar todo

```bash
docker compose up --build -d
```

La primera vez tarda varios minutos porque descarga las imágenes base y compila ambos proyectos.

Una vez levantado, los servicios estarán disponibles en:

| Servicio       | URL                          |
|----------------|------------------------------|
| Frontend       | http://localhost:4321        |
| Backend (API)  | http://localhost:8080        |
| Swagger UI     | http://localhost:8080/docs.html |

---