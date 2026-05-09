# 📖 Guía de Uso: Tu Bóveda de Notas Automatizada

Esta bóveda no es una simple carpeta de archivos; es un sistema visual e interconectado diseñado para que tú te concentres en **aprender y crear**, mientras el código bajo el capó se encarga de organizar, etiquetar y preparar tus espacios de trabajo.

Aquí aprenderás cómo navegar el sistema desde lo más general hasta los detalles del día a día, asegurando que tu grafo de conocimiento crezca de forma ordenada y sin fricción.

---

## 🚀 1. La Filosofía: Escribir de Arriba hacia Abajo

El sistema funciona mejor cuando sigues un flujo "Top-Down" (de lo general a lo particular). En lugar de crear notas sueltas, piensa en ellas como parte de un árbol:

1. **Las Raíces (Notas Estructurales):** Son tus puntos de partida. Un **Tema** de estudio, un **Software** que estás documentando o un **Proyecto** en el que estás trabajando. Estas notas son las que "mandan" y definen el contexto.
    
2. **Las Hojas (Notas Atómicas):** Son piezas pequeñas de información, como un **Concepto** específico, un **Ejercicio** que resolviste o una **Bitácora** de tu sesión.
    

**El secreto:** Si creas una "Hoja" desde adentro de su "Raíz", la nota nueva sabrá automáticamente a qué materia o proyecto pertenece.

---

## 🔗 2. El Proceso de Enlazado Automático

Para que el sistema sea realmente inteligente y conecte tus notas sin que tengas que escribir etiquetas a mano, debes crear las notas atómicas **desde adentro** de su nota padre siguiendo este proceso exacto:

1. **Crea el enlace en tu nota "Padre":** Mientras escribes en tu nota principal (por ejemplo, en el tema "Cálculo Integral"), simplemente menciona el nuevo concepto que quieres crear encerrándolo entre corchetes dobles. Ejemplo: `[[Nombre de mi nuevo concepto]]`.
    
2. **Genera y abre la nota:** Pon el cursor sobre ese enlace que acabas de escribir y presiona **`Ctrl + Enter`** (o haz clic sobre él). Esto creará el archivo en blanco y te llevará directamente adentro.
    
3. **Ejecuta la magia:** Una vez dentro de la nota nueva, presiona **`Alt + E`** para abrir tu menú de plantillas.
    
4. **Elige tu plantilla atómica:** Selecciona "Concepto", "Ejercicio" o "Bitácora".
    
5. **Deja que el script trabaje:** Como creaste la nota a partir del enlace, el sistema leerá tu historial de navegación al instante, sabrá exactamente de qué nota vienes, y le colocará la etiqueta correspondiente a tu nueva nota (ej: `#CalculoIntegral`). Así, tu grafo crece conectado desde el primer segundo.
    

---

## 🛠️ 3. ¿Qué hace el sistema por ti?

Cada vez que aplicas una plantilla, ocurren varias cosas "detrás de escena" para ahorrarte clics:

- **Preparación de Pizarras Visuales:** En plantillas como _Tema_ o _Proyecto_, el sistema te preguntará si quieres crear un mapa mental en Excalidraw. Si dices que sí, lo crea, lo nombra, le inyecta las etiquetas correctas y lo deja listo para dibujar.
    
- **Tableros de Tareas (Kanban):** En los _Proyectos_, se genera automáticamente un tablero visual para que gestiones tus tareas pendientes, en curso y terminadas.
    
- **Salto al Contenido:** Una vez generada la nota, no tienes que usar el mouse. El cursor salta automáticamente al primer encabezado importante para que empieces a escribir de inmediato.
    
- **Orden de Archivos:** Notas como los Proyectos y las Bitácoras se mueven solas a sus carpetas correspondientes para no ensuciar tu vista principal.
    

---

## 📂 4. Organización y Gestión de Carpetas

### Gestión de Materias

Para que el sistema sepa qué materias estás cursando actualmente, debes usar la carpeta **`97-Materias`**.

- **Para agregar una materia:** Simplemente crea una nota vacía dentro de esa carpeta con el nombre de la materia (ej. `Álgebra Lineal`).
    
- A partir de ese momento, cuando crees un nuevo **Tema**, esa materia aparecerá como opción en el menú desplegable.
    

### El flujo Inbox -> Zettelkasten

Para mantener tu sistema limpio y útil, seguimos esta regla:

1. **Bandeja de entrada (Raíz):** Todas las notas nuevas (Conceptos, Ejercicios, Temas) nacen en la carpeta principal de tu bóveda. Considera esto tu zona de "borradores".
    
2. **El archivo final:** Una vez que hayas terminado de escribir la nota y estés satisfecho con su contenido, **muévela manualmente** a la carpeta **`10-Zettelkasten`**. Esto te asegura que todo lo que está guardado allí es conocimiento sólido y revisado.
    

### La Carpeta Data

Es posible que veas una carpeta llamada **`Data`**. No necesitas entrar en ella; es el lugar donde el sistema guarda automáticamente todas las imágenes, capturas de pantalla o PDFs que arrastres hacia tus notas. Su única función es mantener el resto de tus carpetas libres de archivos sueltos.

---

## ⚠️ Advertencias:

Para evitar que las automatizaciones dejen de funcionar, es vital respetar estas restricciones:

1. **No cambies los nombres de las carpetas principales:** Carpetas como `10-Zettelkasten`, `20-Proyectos`, `40-Diagramas`, `97-Materias` y `99-Templates` deben mantener sus nombres exactos, ya que el código las busca así.
    
2. **No renombres las plantillas base:** Los archivos dentro de `99-Templates` (como `Template-Excalidraw.md` o `Template-Kanban-Software.md`) son los "moldes" del sistema. Si les cambias el nombre, los scripts no encontrarán qué copiar.
    
3. **Mantén los Tags al final de la nota:** El motor inteligente busca las etiquetas leyendo la **última línea** de tus notas de texto. Asegúrate de no escribir contenido debajo de la línea que dice `Tags: #...`.