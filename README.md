# Temario de Aplicaciones Web

# 1. Introducción al Desarrollo Web
## Historia y Evolución del Desarrollo Web

El desarrollo web ha experimentado una evolución vertiginosa desde sus inicios en la década de los 90:

- **Década de 1990:**  
  - *1990:* Tim Berners-Lee crea la World Wide Web.
  - *1993-1995:* Primeros navegadores gráficos (Mosaic, Netscape Navigator).
  - Las páginas web eran estáticas, compuestas principalmente por HTML simple.

- **Finales de los 90 y principios de los 2000:**  
  - Introducción de CSS y JavaScript, permitiendo páginas más interactivas y estilizadas.
  - Aparición de lenguajes de servidor como PHP, ASP y bases de datos como MySQL, lo que dio paso a páginas dinámicas.

- **Década de 2010 en adelante:**  
  - Auge de frameworks y bibliotecas como jQuery, Angular, React y Vue.js.
  - Popularidad de aplicaciones de una sola página (SPA) y aplicaciones progresivas (PWA).
  - El desarrollo web se orienta a la experiencia del usuario, rendimiento y accesibilidad.

## Tipos de Aplicaciones Web

A lo largo de esta evolución, han surgido varios tipos de aplicaciones web:

### 1. Aplicaciones Web Estáticas

- **Características:**  
  - El contenido no cambia en función del usuario o la interacción.
  - Compuestas principalmente por archivos HTML, CSS y a veces JavaScript.
  - Ejemplo: Sitios web informativos o portafolios personales.

### 2. Aplicaciones Web Dinámicas

- **Características:**  
  - El contenido se genera dinámicamente en el servidor o en el cliente según la interacción o la base de datos.
  - Utilizan lenguajes como PHP, Python, Ruby, Node.js.
  - Ejemplo: Tiendas en línea, foros, sistemas de gestión de contenido (CMS).

### 3. SPA (Single Page Application / Aplicación de Página Única)

- **Características:**  
  - Cargan una sola página HTML y actualizan dinámicamente el contenido conforme el usuario interactúa.
  - Utilizan frameworks/librerías como React, Angular o Vue.js.
  - Mejoran la experiencia del usuario al evitar recargas completas de página.
  - Ejemplo: Gmail, Facebook.

### 4. PWA (Progressive Web Application / Aplicación Web Progresiva)

- **Características:**  
  - Aplicaciones web que utilizan capacidades modernas del navegador para ofrecer una experiencia similar a una aplicación nativa.
  - Funcionan offline, pueden instalarse en el dispositivo y enviar notificaciones.
  - Utilizan tecnologías como Service Workers, manifest.json.
  - Ejemplo: Twitter Lite, Starbucks PWA.

---
# 2. Arquitectura de Aplicaciones Web

## Cliente-Servidor

La **arquitectura cliente-servidor** es la base del desarrollo web moderno. Consiste en dos partes principales:

- **Cliente:**  
  - Es la aplicación o navegador desde donde el usuario interactúa.  
  - Solicita recursos o servicios al servidor (por ejemplo, cargar una página web).

- **Servidor:**  
  - Es el sistema que responde a las solicitudes del cliente.  
  - Procesa datos, ejecuta lógica de negocio y envía respuestas (como páginas HTML, datos JSON).

**Ejemplo:** Cuando accedes a www.ejemplo.com desde tu navegador (cliente), el servidor web responde enviando los archivos necesarios para visualizar la página.

## Arquitectura de Tres Capas

La **arquitectura de tres capas** (Three-tier architecture) es un modelo que separa una aplicación en tres niveles independientes:

1. **Capa de Presentación (Frontend):**
   - Interfaz gráfica que ve el usuario.
   - Normalmente compuesta por HTML, CSS, JavaScript, y frameworks como React, Angular, Vue.js.

2. **Capa de Lógica (Backend o lógica de negocio):**
   - Procesa la lógica de la aplicación.
   - Puede estar desarrollada en Node.js, Python, Java, etc.
   - Gestiona reglas de negocio, autenticación, autorización, etc.

3. **Capa de Datos (Base de datos):**
   - Donde se almacenan y gestionan los datos.
   - Uso de sistemas como MySQL, PostgreSQL, MongoDB, etc.

**Ventajas:**
- Separación de responsabilidades.
- Escalabilidad y facilidad de mantenimiento.

## REST y API-first Design

### REST (Representational State Transfer)

- Es un estilo de arquitectura para diseñar servicios web.
- Utiliza HTTP y sus métodos (GET, POST, PUT, DELETE) para realizar operaciones sobre recursos identificados mediante URLs.
- Las respuestas suelen ser en formato JSON o XML.

**Ejemplo de endpoints REST:**
- `GET /usuarios` — obtiene todos los usuarios.
- `POST /usuarios` — crea un nuevo usuario.

### API-first Design

- Estrategia de desarrollo donde se diseña la **API** antes de implementar la lógica de la aplicación.
- Permite definir contratos claros entre el frontend y el backend mediante especificaciones (OpenAPI/Swagger).
- Facilita el trabajo paralelo entre equipos, mejora la documentación y la mantenibilidad.
---
# 3. Lenguajes y Tecnologías Fundamentales

El desarrollo web se apoya en varios lenguajes y tecnologías esenciales. Entre los más importantes destacan:

## HTML (HyperText Markup Language)

- Es el lenguaje de marcado principal para la creación de páginas web.
- Define la estructura y el contenido de la web utilizando etiquetas (`<html>`, `<head>`, `<body>`, `<h1>`, `<p>`, etc.).
- Todos los sitios web usan HTML como base.

**Ejemplo:**
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Mi Página Web</title>
  </head>
  <body>
    <h1>¡Hola, mundo!</h1>
    <p>Bienvenido a mi sitio web.</p>
  </body>
</html>
```

## CSS (Cascading Style Sheets)

- Es el lenguaje de estilos que da formato y diseño a los documentos HTML.
- Permite separar la estructura (HTML) de la presentación (CSS).
- Controla colores, fuentes, márgenes, disposición, animaciones, etc.

**Ejemplo:**
```css
body {
  background-color: #f0f0f0;
  color: #222;
  font-family: Arial, sans-serif;
}

h1 {
  color: #007bff;
}
```

## JavaScript

- Lenguaje de programación principal en el lado del cliente (frontend).
- Permite crear páginas web interactivas, validar formularios, manipular el DOM, realizar peticiones asíncronas (AJAX), etc.
- También se utiliza en el backend mediante Node.js.

**Ejemplo:**
```javascript
document.getElementById('btnSaludar').onclick = function() {
  alert('¡Hola desde JavaScript!');
};
```

## PHP

- Lenguaje de programación del lado del servidor, ampliamente usado para crear aplicaciones web dinámicas.
- Permite interactuar con bases de datos, gestionar sesiones, enviar correos, etc.
- Es base de muchos CMS populares como WordPress, Joomla y Drupal.

**Ejemplo:**
```php
<?php
  echo "¡Hola desde PHP!";
?>
```

## MySQL

- Sistema de gestión de bases de datos relacional (RDBMS) muy popular en el desarrollo web.
- Utiliza el lenguaje SQL para crear, leer, actualizar y eliminar datos de la base de datos.
- Se integra fácilmente con PHP y otras tecnologías backend.

**Ejemplo:**
```sql
SELECT nombre, correo FROM usuarios WHERE activo = 1;
```

---
