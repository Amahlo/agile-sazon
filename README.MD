# Agile Sazón 🍲

Bienvenido al repositorio central del proyecto **Agile Sazón**. Este documento define las pautas de colaboración, entrega de documentación y metodología de trabajo con Git para todos los líderes e integrantes de equipo.

---

## 📌 1. Directrices Generales para Líderes y Equipos

### 🍴 Fork del Repositorio
* **Cada líder de equipo/módulo debe forkear** este repositorio oficial en su cuenta de GitHub/GitLab.
* El trabajo del equipo se desarrollará sobre dicho fork y se sincronizará periódicamente mediante Pull Requests hacia el repositorio principal.

### 📄 Documentación Requerida por Módulo
Dentro de la carpeta de cada módulo asignado (ubicados en `src/`), el equipo debe adjuntar la documentación técnica y de gestión correspondiente:
* **Backlog:** Historias de usuario, requerimientos funcionales y no funcionales, criterios de aceptación y priorización (Sprint Backlog).
* **Informe:** Documento descriptivo del módulo, objetivos, alcance, decisiones arquitectónicas, estado actual y conclusiones.
* **Wireframes:** Bocetos o prototipos de interfaz de usuario (UI/UX), diagramas de flujo y navegación.

---

## 👥 2. Perfil y Biografía de Integrantes por Carpeta

Cada carpeta de módulo debe contar de manera obligatoria con su propio archivo `README.md` local, el cual incluirá la información detallada de cada integrante del equipo a modo de biografía:

* **Nombre completo y Rol:** (ej. Líder de Módulo, Frontend Dev, Backend Dev, QA, UI/UX Designer).
* **Experiencia:** Trayectoria profesional, formación académica y proyectos previos relevantes.
* **Capacidades y Fortalezas:** Habilidades técnicas (lenguajes, frameworks, herramientas), metodologías y habilidades blandas.
* **Información Relevante:** Datos de contacto, enlaces a LinkedIn/GitHub y aportes particulares dentro del módulo.

#### Estructura sugerida para el `README.md` de cada módulo:
```markdown
# Módulo: [Nombre del Módulo]

## 📋 Documentación
- [Backlog](./docs/backlog.md)
- [Informe](./docs/informe.md)
- [Wireframes](./docs/wireframes/)

## 👨‍💻 Integrantes del Equipo

### [Nombre del Integrante 1] - [Rol]
- **Experiencia:** ...
- **Capacidades:** ...
- **Contacto / Redes:** ...

### [Nombre del Integrante 2] - [Rol]
- **Experiencia:** ...
- **Capacidades:** ...
- **Contacto / Redes:** ...
```

---

### Ramas Principales

| Rama | Descripción |
| :--- | :--- |
| **`main`** | Contiene el código en estado de producción, probado y 100% estable. Solo recibe fusiones de ramas `release` o `hotfix`. |
| **`develop`** | Rama base para la integración continua de todas las funcionalidades terminadas. |

### Ramas de Soporte

* **`feature/<nombre-funcionalidad>`**:
  * Se desprenden de: `develop`
  * Se fusionan en: `develop`
  * Uso: Para el desarrollo de módulos o tareas específicas. Ningún desarrollador debe subir cambios directamente a `develop` o `main`.
* **`release/<version>`**:
  * Se desprenden de: `develop`
  * Se fusionan en: `main` y `develop`
  * Uso: Preparación y estabilización para una nueva versión de entrega.
* **`hotfix/<nombre-arreglo>`**:
  * Se desprenden de: `main`
  * Se fusionan en: `main` y `develop`
  * Uso: Correcciones críticas y urgentes en producción.

---

## 📂 Estructura de Módulos (`src/`)

```text
src/
├── autenticacion/     # Gestión de accesos, roles y registro
├── catalogo/          # Catálogo de productos/ingredientes
├── comunidad/         # Foros, recetas compartidas y valoraciones
├── despensa/          # Gestión de inventario de cocina/despensa
├── mercadeo/          # Campañas, promociones y métricas
├── nutricion/         # Información nutricional, planes y dietas
├── planificador/      # Planificación de menús y compras
└── recetario/         # Gestión y preparación de recetas
```
