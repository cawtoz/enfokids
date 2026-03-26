# Cómo ejecutar EnfoKids

## Requisito

Tener instalado **Docker Desktop**: https://www.youtube.com/watch?v=IMqYPAwX3iM

## Pasos

**1. Abrir una terminal en la carpeta `enfokids`**

**2. Ejecutar el proyecto**

```bash
docker compose up --build
```

Esto descarga las imágenes, construye el proyecto y levanta todo. La primera vez tarda unos minutos.

**3. Abrir el navegador**

```
http://localhost:4321
```

## Usuarios de prueba

| Correo | Contraseña | Rol |
|---|---|---|
| admin@example.com | adminpass | Administrador |
| therapist@example.com | therapistpass | Terapeuta |
| caregiver@example.com | caregiverpass | Cuidador |
| child@example.com | childpass | Niño |

## Detener el proyecto

```bash
docker compose down
```

**Importante:** Los datos de prueba solo se cargan una vez. Después de la primera ejecución, abrir el archivo `.env` y cambiar:

```
APP_DATA_INIT=true  →  APP_DATA_INIT=false
```

Luego se puede volver a ejecutar normalmente y no se van a duplicar los datos:

```bash
docker compose up --build
```
