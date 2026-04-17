# Evolution API - Self Hosted

## Configuración Inicial

Antes de iniciar, **IMPORTANTE**: edita el archivo `.env` y cambia:
- `AUTHENTICATION_API_KEY`: Cambia `change-this-to-a-secure-random-key` por una clave segura
- `MONGODB_PASSWORD`: Cambia `rootpassword` por una contraseña segura

## Comandos

### Iniciar los servicios
```bash
docker-compose up -d
```

### Ver logs
```bash
docker-compose logs -f evolution-api
```

### Detener los servicios
```bash
docker-compose down
```

### Detener y eliminar volúmenes (limpieza completa)
```bash
docker-compose down -v
```

## Acceso

La API estará disponible en: `http://localhost:8080`

## Documentación de la API

Una vez iniciado, accede a la documentación Swagger en:
`http://localhost:8080/docs`

## Autenticación

Todas las peticiones a la API requieren el header:
```
apikey: tu-api-key-configurada-en-env
```

## Estructura de Volúmenes

- `evolution_instances`: Almacena las instancias de WhatsApp
- `evolution_store`: Almacena archivos y media
- `mongodb_data`: Base de datos MongoDB
- `redis_data`: Cache de Redis
