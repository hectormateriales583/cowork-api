# Cowork API

## Arrancar el proyecto desde IntelliJ

Ejecutar desde la terminal:

```bash
.\mvnw spring-boot:run
```

La aplicación se ejecuta en:

```plaintext
http://localhost:9090
```

---

# Información de la API

| Método | Ruta | Descripción |
|---|---|---|
| GET | /api/info | Devuelve metadatos básicos de la aplicación (nombre, versión, autor). |
| GET | /api/salas | Lista todas las salas registradas. |
| GET | /api/salas/{id} | Obtiene el detalle de una sala por su ID. |
| POST | /api/salas | Crea una nueva sala. |
| PUT | /api/salas/{id} | Actualiza los datos de una sala existente. |
| DELETE | /api/salas/{id} | Elimina una sala y aplica borrado en cascada sobre sus reservas asociadas. |
| GET | /api/reservas | Lista reservas aplicando filtros opcionales. |
| GET | /api/reservas/{id} | Obtiene el detalle de una reserva por su ID. |
| GET | /api/reservas/sala/{salaId} | Obtiene reservas asociadas a una sala. |
| POST | /api/reservas | Registra una nueva reserva. |
| PUT | /api/reservas/{id}/estado | Cambia el estado de una reserva. |
| DELETE | /api/reservas/{id} | Elimina una reserva del sistema. |
| POST | /api/reservas/{id}/comprobante | Sube un archivo PDF comprobante. |

---

# Responsabilidad de cada capa

| Capa | Descripción |
|---|---|
| controller | Recibe peticiones HTTP, valida parámetros y devuelve respuestas JSON. |
| service | Contiene lógica de negocio y validaciones. |
| repository | Gestiona datos en memoria usando List y AtomicLong. |
| model | Representa entidades del dominio. |
| dto | Define contratos de entrada y salida. |
| mapper | Convierte model a dto y viceversa. |

---

# Capturas de pantalla

## Aplicación ejecutándose en puerto 9090

![Puerto 9090](docs/puerto9090.png)

---

## Endpoint GET /api/info

![API INFO](docs/api-info.png)

---

## Endpoint GET /api/salas

![API SALAS](docs/api-salas.png)

---

## Endpoint PUT /api/salas

![PUT SALAS](docs/put-salas.png)

---

## Eliminación de sala

![DELETE SALAS](docs/delete-salas.png)

---

# Tecnologías utilizadas

- Java 17
- Spring Boot
- Maven
- Postman
- GitHub

---

# Repositorio GitHub

https://github.com/hectormateriales583/cowork-api
