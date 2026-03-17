#  Proyecto Cats Gallery

##  Descripción

Aplicación web desarrollada con React que permite visualizar contenido multimedia (imágenes, PDFs y videos) almacenado en Azure Storage.

---

##  Arquitectura

El proyecto está estructurado en **capas (layers)**:

### Presentation Layer

Encargada de la interfaz de usuario.

* React + Vite + Tailwind
* Componentes:

  * catCard.jsx
  * catDetails.jsx
* Páginas:

  * Gallery.jsx

---

### Application Layer

Contiene la lógica de la aplicación.

* Hooks:

  * useCats.js → maneja estado y lógica de consumo
* Services:

  * catService.js → acceso a datos

---

### Data Layer

Encargada del almacenamiento.

* Azure Storage Account:

  * imágenes
  * PDFs
  * videos

---

##  Flujo de datos

Usuario → UI → Hooks → Services → Azure Storage

---

##  Patrones utilizados

* **Separación por capas**

  * Divide responsabilidades entre UI, lógica y datos

* **Custom Hooks**

  * Encapsulan lógica reutilizable

* **Service Layer**

  * Centraliza el acceso a datos

---

##  Principios SOLID aplicados

* **Single Responsibility Principle**

  * Cada archivo tiene una única responsabilidad

* **Open/Closed Principle**

  * Se pueden agregar nuevos servicios sin modificar la UI

* **Dependency Inversion**

  * La UI depende de hooks, no directamente de servicios

---

## CI/CD

El proyecto utiliza GitHub para control de versiones y despliegue en Azure:

* **CI (Integración continua)**

  * Validación de código y build

* **CD (Despliegue continuo)**

  * Publicación automática en Azure Web App

---

## Tecnologías

* React
* Vite
* TailwindCSS
* Azure Storage
* GitHub

---

## 📌 Conclusión

El proyecto implementa una arquitectura por capas que permite escalabilidad, mantenimiento y separación clara de responsabilidades.

