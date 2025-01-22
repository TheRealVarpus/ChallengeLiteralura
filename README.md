# **LiterAlura**

LiterAlura es una aplicación que permite administrar y explorar información sobre libros y autores, conectándose con datos de una API externa. Ofrece herramientas para buscar, registrar y listar libros y autores según diferentes criterios.

## **Características Principales**

- **Búsqueda de libros por título:** Obtiene libros desde la API externa y los almacena en la base de datos.
- **Gestión de registros:** Muestra la lista de libros y autores registrados.
- **Filtrado por criterios:**
  - Autores vivos en un año específico.
  - Libros organizados por idioma (español, inglés, francés, entre otros).

---

## **Requisitos Previos**

Antes de comenzar, verifica que tienes lo siguiente instalado en tu sistema:

- **Java 17** o superior.
- **Maven 3.8.1** o superior.
- **MySQL 8.0** o una versión compatible.

---

## **Instalación y Configuración**

### **1. Clonar el Repositorio**

```bash
git clone https://github.com/TheRealVarpus/ChallengeLiteralura.git
cd ChallengeLiterAlura
```

### **2. Configurar Variables de Entorno**

Define las siguientes variables para conectar la aplicación con tu base de datos:

| Variable      | Descripción                  | Ejemplo        |
|---------------|------------------------------|----------------|
| DB_HOST       | Dirección del servidor       | localhost      |
| DB_PORT       | Puerto de conexión           | 3306           |
| DB_NAME       | Nombre de la base de datos   | LiterAlura  |
| DB_USERNAME   | Usuario de la base de datos  | root           |
| DB_PASSWORD   | Contraseña de la base de datos | tu_contraseña |

También puedes configurar estas credenciales en `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/LiterAlura
spring.datasource.username=root
spring.datasource.password=tu_contraseña
```

### **3. Crear la Base de Datos**

Ejecuta el siguiente comando para crear la base de datos necesaria:

```sql
CREATE DATABASE gestor_libros;
```

### **4. Construir el Proyecto**

Compila el proyecto y descarga las dependencias necesarias con:

```bash
mvn clean install
```

---

## **Ejecución**

1. Ejecuta la aplicación:
   ```bash
   mvn spring-boot:run
   ```

2. Utiliza el menú interactivo para acceder a las funcionalidades principales:

```plaintext
1 - Buscar libro por título
2 - Listar libros registrados
3 - Listar autores registrados
4 - Autores vivos en un año específico
5 - Listar libros por idioma
0 - Salir
```

---

## **Tecnologías Utilizadas**

- **Java 17**
- **Spring Boot 3.x**
- **Spring Data JPA**
- **MySQL** (Base de datos relacional)
- **Librerías para manejo de JSON**

---

## **Estructura del Proyecto**

```plaintext
src
+-- main
¦   +-- java/com/miempresa/gestorlibros
¦   ¦   +-- main/Aplicacion.java         # Clase principal
¦   ¦   +-- repositorio                 # Repositorios JPA
¦   ¦   +-- servicio                    # Servicios para lógica de negocio
¦   ¦   +-- modelo                      # Clases modelo: Autor, Libro
¦   +-- resources
¦       +-- application.properties      # Configuración de la aplicación
+-- test                                 # Pruebas unitarias
```

---

## **Contribuciones**

¡Tu ayuda es bienvenida! Sigue estos pasos para contribuir:

1. Realiza un fork del proyecto.
2. Crea una nueva rama: `git checkout -b nueva-funcionalidad`.
3. Realiza tus cambios y súbelos: `git commit -m "Descripción de los cambios"`.
4. Envía tus cambios al repositorio remoto: `git push origin nueva-funcionalidad`.
5. Abre un Pull Request.

---

¡Gracias por utilizar LiterAlura! 

