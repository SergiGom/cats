# Proyecto Cats Gallery

## Descripción

Esta es una aplicación web hecha con React que permite visualizar contenido multimedia (imágenes, PDFs y videos) almacenado en Azure Storage. La idea principal es mostrar una galería sencilla donde el usuario pueda explorar este contenido.

---

## Estructura del proyecto

El proyecto está organizado en diferentes capas para separar responsabilidades y mantener el código más ordenado.

### Presentation Layer

Aquí está todo lo relacionado con la interfaz:

* React + Vite + Tailwind
* Componentes como:

  * catCard.jsx
  * catDetails.jsx
* Página principal:

  * Gallery.jsx

Esta capa solo se encarga de mostrar la información al usuario.

---

### Application Layer

Aquí se maneja la lógica de la aplicación:

* useCats.js
  Se encarga de manejar el estado y consumir los datos

* catService.js
  Se encarga de traer la información desde Azure

Esta capa conecta la interfaz con los datos.

---

### Data Layer

Aquí está el almacenamiento:

* Azure Storage Account

  * imágenes
  * PDFs
  * videos

---

## Flujo de la aplicación

El flujo es bastante directo:

Usuario → Interfaz → Hook → Servicio → Azure Storage

---

## Decisiones de diseño

Se separó el código en capas para que cada parte tenga una responsabilidad clara.
Por ejemplo:

* Los componentes solo muestran datos
* Los hooks manejan lógica
* Los servicios acceden a los datos

Esto hace que el proyecto sea más fácil de mantener y entender.

---

## Principios aplicados

No es una implementación estricta de SOLID, pero sí se aplican algunas ideas:

* Cada archivo tiene una responsabilidad específica
* La UI no accede directamente a los datos
* La lógica está separada de la presentación

---

## CI/CD

El proyecto se maneja con GitHub y se desplegó en Azure.

* Se usa Git para control de versiones
* El despliegue se realiza hacia Azure Web App

(No hay un pipeline complejo, pero se sigue un flujo básico de integración y despliegue)

---

## Tecnologías usadas

* React
* Vite
* Tailwind CSS
* Azure Storage
* GitHub

---

## Comentario final

El proyecto está pensado como una base sencilla pero organizada.
Aunque es una aplicación pequeña, se intentó mantener una estructura que permita escalar o agregar nuevas funcionalidades sin desordenar el código.
