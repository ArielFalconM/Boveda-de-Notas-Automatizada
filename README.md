# 🚀 Boveda de Notas Automatizada

Este repositorio es un **Entorno de Conocimiento Visual Automatizado** basado en la metodología Zettelkasten. A diferencia de los sistemas tradicionales de apuntes estáticos, esta bóveda fusiona el pensamiento visual orgánico (diagramas interactivos, imágenes y tableros) con una sólida arquitectura de enlaces gestionada por código.

El sistema integra lógica de programación en **JavaScript** mediante el plugin **Templater**, interactuando con la **API de Obsidian** para automatizar la creación de recursos, la categorización de información y la generación de espacios de trabajo visuales (Excalidraw y Kanban). 

## 📦 Instalación

1. **Generar tu Repositorio:** Utiliza el botón **"Use this template"** en GitHub para clonar este entorno con un historial limpio.
2. **Despliegue en Obsidian:** Abre la carpeta como una bóveda (Vault) desde la aplicación.
3. **Confianza en el Código:** Al ser un sistema que ejecuta scripts, es necesario **"Desactivar el Modo Seguro"** (Trust author and turn off Safe Mode). Esto permite que el motor de Templater procese la lógica de los archivos de la carpeta `.obsidian/`.

## ⚙️ Workflow y Arquitectura de Conexiones

La arquitectura de este motor está diseñada para ser "Context-Aware" (consciente del contexto), eliminando la necesidad de que el usuario decida dónde guardar o cómo enlazar una nota. Los scripts detectan el estado actual de la interfaz para heredar metadatos.

### Flujos de Trabajo Automatizados

* **Inventario Tecnológico y Stack Dinámico:** Las notas de **Software** funcionan como un inventario de infraestructura. Al crear un **Proyecto**, el sistema escanea el vault, filtra los archivos por tags de software y permite construir el *Stack Tecnológico* mediante un menú de selección interactivo.
* **Gestión de Ciclo de Vida de Proyectos:** Al instanciar un proyecto, el script ejecuta un despliegue múltiple: mueve la nota a la carpeta correspondiente, clona un tablero **Kanban** técnico y genera una pizarra de **Excalidraw** para arquitectura.
* **Trazabilidad de Sesiones (Bitácoras):** Lo ideal es generar las **Bitácoras** mientras se trabaja en la nota del proyecto; así, el script detecta automáticamente el contexto a través de *backlinks* o historial reciente y vincula la sesión sin intervención manual.
* **Ecosistema Académico (Tema y Práctico):** Al crear un **Práctico** desde una nota de **Tema**, el sistema no solo hereda el nombre de la materia, sino que establece un puente directo entre el pizarron de resolución nuevo y el pizarron teórico preexistente.
* **Captura Atómica de Conceptos:** Se recomienda crear los **Conceptos** desde su nota padre (un Tema o Software). El script utiliza el historial de navegación para sugerir y establecer el origen de la nota automáticamente.

### Activos Generados por Template

| Template | Automatización Destacada |
| :--- | :--- |
| **🚀 Proyecto** | Despliegue de tablero Kanban y pizarra técnica. Selección dinámica de Stack basada en tags. |
| **💻 Software** | Categorización técnica y preparación de metadatos para el motor de proyectos. |
| **✏️ Práctico** | Generación de pizarra de resolución vinculada por referencia al mapa teórico del Tema. |
| **🎓 Tema** | Creación de Pizarra de Teoría en la carpeta de diagramas y clasificación por materia académica. |
| **📔 Bitácora** | Vinculación automática con el mapa del proyecto y checklist de fin de sesión para control de cambios. |

## 🛠️ Detalles de Implementación Técnica

* **Bypass de Foco:** Todos los scripts implementan una función asíncrona que, tras realizar el `rename` y `move` del archivo, fuerza el foco del cursor en la primera línea de contenido relevante, optimizando el tiempo de respuesta del usuario.
* **Integración de UI:** Se utilizan los métodos `tp.system.suggester` y `tp.system.prompt` para crear una interfaz de usuario fluida que interactúa con el sistema de archivos de Obsidian en tiempo real.
* **Leyendas Técnicas:** Los tableros Kanban incluyen una leyenda de colores específica para flujos de ingeniería: `#bug` (rojo), `#feature` (verde), `#refactor` (azul) y `#test` (amarillo).

## ⚠️ Observaciones para el Usuario

* **Configuración de Listas:** Muchas opciones (como las materias en **Tema** o categorías en **Software**) están hardcodeadas en los archivos de la carpeta `99-Templates/`. Es necesario editar el código JavaScript dentro de estos Markdown para personalizar los arrays de opciones.
* **Estructura de Directorios:** Los scripts requieren que las carpetas `10-Zettelkasten`, `20-Proyectos`, `40-Diagramas` y `99-Templates` mantengan sus nombres originales, ya que son utilizados como constantes para las operaciones de IO de los templates.
