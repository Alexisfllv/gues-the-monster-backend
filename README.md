# 🧟‍♂️ Proyecto Monstruos API

API REST para la gestión de monstruos, desarrollada con **Spring Boot**, utilizando **Spring Web**, **Spring Data JPA**, **Lombok**, **MapStruct** y **PostgreSQL**.

---

## 🧩 Tecnologías utilizadas

- **Java 17**
- **Spring Boot**
  - Spring Web
  - Spring Data JPA
- **PostgreSQL**
- **Lombok**
- **MapStruct**
- **Maven**

---

## 🗄️ Modelo de Datos

Representación ASCII de la tabla principal:

```
+------------------+
|    MONSTRUO      |
+------------------+
| id              | SERIAL (PK, AUTOINCREMENT) |
| nombre          | VARCHAR                    |
| imagen_silueta  | VARCHAR (URL o ruta)       |
| imagen_real     | VARCHAR (URL o ruta)       |
+------------------+
```

---

## 🧠 Estructura del Proyecto

```
src/main/java/com/tuempresa/monstruos
│
├── controller      # Controladores REST
├── service         # Lógica de negocio
├── repository      # Interfaces JPA
├── entity          # Entidades JPA
├── dto             # Clases DTO
└── mapper          # MapStruct mappers
```

---

## ⚙️ Configuración

Archivo `application.properties` ejemplo:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/monstruosdb
spring.datasource.username=postgres
spring.datasource.password=tu_contraseña
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

---

## 🚀 Ejecución

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tuusuario/monstruos-api.git
   ```

2. Compila y ejecuta:
   ```bash
   mvn spring-boot:run
   ```

3. La API estará disponible en:
   ```
   http://localhost:8080/api/monstruos
   ```

---

## 🧾 Endpoints esperados (ejemplo)

| Método | Endpoint               | Descripción                  |
|--------|------------------------|------------------------------|
| GET    | /api/monstruos         | Lista todos los monstruos    |
| GET    | /api/monstruos/{id}    | Obtiene un monstruo por ID   |
| POST   | /api/monstruos         | Crea un nuevo monstruo       |
| PUT    | /api/monstruos/{id}    | Actualiza un monstruo        |
| DELETE | /api/monstruos/{id}    | Elimina un monstruo          |

---

## 🧰 Dependencias principales (pom.xml)

```xml
<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-data-jpa</artifactId>
    </dependency>
    <dependency>
        <groupId>org.postgresql</groupId>
        <artifactId>postgresql</artifactId>
    </dependency>
    <dependency>
        <groupId>org.projectlombok</groupId>
        <artifactId>lombok</artifactId>
        <optional>true</optional>
    </dependency>
    <dependency>
        <groupId>org.mapstruct</groupId>
        <artifactId>mapstruct</artifactId>
        <version>1.5.5.Final</version>
    </dependency>
</dependencies>
```

---
---
