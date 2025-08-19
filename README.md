# 🖥️ AREP - Servidor HTTP Simple en Java

Este proyecto implementa un **servidor HTTP ligero en Java** desarrollado como parte del curso de Arquitectura de Redes y Aplicaciones (AREP).

El servidor permite:

- Servir archivos estáticos (HTML, CSS, JS, imágenes).
- Exponer endpoints REST (`/hello` y `/hellopost`).
- Manejar parámetros en la URL (query params).
- Ejecutar múltiples solicitudes de manera secuencial (no concurrente).

No se utilizan frameworks web como Spring o Spark, solo Java estándar y las librerías de red.

---

## 📂 Estructura del Proyecto

```text
.
├── src
│   ├── main
│   │   ├── java
│   │   │   └── edu
│   │   │       └── escuelaing
│   │   │           └── app
│   │   │               ├── SimpleHttpServer.java   # Clase principal: servidor HTTP
│   │   │               ├── MimeTypes.java          # Detecta tipos MIME
│   │   │               └── UrlUtils.java           # Utilidad para parsear URLs
│   │   └── resources
│   │       └── public                              # Archivos estáticos
│   │           ├── index.html
│   │           ├── app.js
│   │           ├── style.css
│   │           └── images/
│   └── test
│       └── java
│           └── edu
│               └── escuelaing
│                   └── app
└── target                                           # Archivos generados por Maven
```

⚙️ Requisitos

-Java 17+

-Maven 3.8+

-Git

Verifica versiones instaladas:
```bash
java -version
mvn -v
```

🚀 Ejecución

Clonar el repositorio:
```bash
git clone https://github.com/usuario/AREP.git
cd AREP
```

Compilar el proyecto con Maven:
```bash
mvn clean install
```

Ejecutar el servidor:
```bash
mvn exec:java
```

Abrir en el navegador:
```bash
http://localhost:8080/
```

✅ Pruebas

Ejecutar los tests unitarios:
```bash
mvn test
```

🌐 Endpoints Disponibles
1. GET /hello?name=TuNombre

-Hello TuNombre!

2. POST /hellopost?name=TuNombre

-Hello POST TuNombre!

📦 Empaquetado y Despliegue

Generar .jar ejecutable:
```bash
mvn package
```

Ejecutar el .jar:
```bash
java -cp target/AREP-1.0.0.jar edu.escuelaing.app.SimpleHttpServer
```

🛠️ Tecnologías

-Java 17 - Lenguaje principal

-Maven - Gestión de dependencias y build

-JUnit 4 - Testing framework

✒️ Autor

Proyecto desarrollado por:
Santiago Arteaga - GitHub

