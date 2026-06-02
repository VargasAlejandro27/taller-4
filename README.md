# API REST de Estudiantes con Spring Boot

Este proyecto implementa una API REST con **Spring Boot**, **Kotlin**, **Spring Data JPA** y **H2** para gestionar estudiantes.

## Objetivo

- Crear estudiantes.
- Listar todos los estudiantes registrados.

## Estructura del proyecto

- `src/main/kotlin/com/pucetec/students/controllers` - controladores REST.
- `src/main/kotlin/com/pucetec/students/services` - lógica de negocio.
- `src/main/kotlin/com/pucetec/students/repositories` - acceso a datos con Spring Data JPA.
- `src/main/kotlin/com/pucetec/students/entities` - entidad `Student`.
- `src/main/kotlin/com/pucetec/students/dto` - DTOs para peticiones y respuestas.
- `src/main/resources/application.yaml` - configuración de H2 y JPA.

## Entidad `Student`

La entidad tiene únicamente los campos:

- `id: Long`
- `name: String`
- `email: String`

## Endpoints

- `POST /students`
  - Crea un estudiante.
  - Body ejemplo:
    ```json
    {
      "name": "Ana Torres",
      "email": "ana.torres@email.com"
    }
    ```
- `GET /students`
  - Lista todos los estudiantes registrados.

## Configuración H2

La base de datos en memoria H2 está habilitada en `application.yaml`.

- URL JDBC: `jdbc:h2:mem:studentsdb`
- Consola H2: `http://localhost:8787/h2-console`
- Usuario: `admin`
- Contraseña: `admin`

## Ejecución

1. Ejecutar la aplicación con Gradle:
   ```bash
   ./gradlew bootRun
   ```
2. Probar los endpoints con Postman, Insomnia o curl.

## Pruebas y documentación

- Esta implementación sigue los requisitos de la tarea: Spring Boot + Kotlin, Gradle, H2, Spring Data JPA, capas `controller` / `service` / `repository`, entidad `Student`, y uso de DTOs.
- Se documentaron los endpoints y la configuración de H2 en este README.
