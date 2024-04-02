
# API de Usuarios

Esta API proporciona endpoints para la gestión de usuarios.

## Instalación

Para instalar las dependencias del proyecto, ejecuta el siguiente comando:

```bash
composer install
```

## Iniciar el servidor

Para iniciar el servidor, ejecuta el siguiente comando:

```bash
php -S localhost:8000 -t ./public
```

## Métodos Disponibles

### GET `/api/users`

Este endpoint devuelve todos los usuarios almacenados en la base de datos.

Ejemplo de uso:

```bash
curl http://localhost:8000/api/users
```

### GET `/api/users/{id}`

Este endpoint devuelve un usuario específico almacenado en la base de datos.

Ejemplo de uso:

```bash
curl http://localhost:8000/api/users/1
```

### POST `/api/users`

Este endpoint crea un nuevo usuario en la base de datos.

Ejemplo de uso:

```bash
curl -X POST -H "Content-Type: application/json" -d '{"name":"Goizane", "email":"goizane@gmail.com"}' http://localhost:8000/api/users
```
Otra forma de hacerlo es con el comando:
```bash
curl -d "name=Goizane&email=goizane@gmail.com" http://localhost:8000/api/users
```

### PUT `/api/users/{id}`

Este endpoint actualiza un usuario específico almacenado en la base de datos.

Ejemplo de uso:

```bash
curl -X PUT -d  "name=Goizane2&email=goizane2@gmail.com" http://localhost:8000/api/users/1
```
Otra forma de hacerlo es con el comando:
```bash
curl -X PUT -H "Content-Type: application/json" -d '{"name":"Goizane2", "email":"goizane2@example.com"}' http://localhost:8000/api/users/1
```

### DELETE `/api/users/{id}`

Este endpoint elimina un usuario específico almacenado en la base de datos.


Ejemplo de uso:

```bash
curl -X DELETE http://localhost:8000/api/users/1
```