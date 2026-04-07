# 📋 Planificación de Tareas: MVP SIASE Mejorado

¡Bienvenidos al proyecto! En este documento listamos las tareas necesarias para lanzar el primer *Minimum Viable Product (MVP)* en menos de una semana. Con un equipo de 4 personas, estas tareas pueden distribuirse ágilmente.

Para mantener la organización, cuando alguien elija una tarea, deberá comunicarlo (por ejemplo, en el grupo de WhatsApp) y si es posible, asignar su nombre junto a ella en el tablero de GitHub.

## Fase 1: 🎨 Diseño y UX (User Experience)
*Diseño visual sin tocar código todavía. El objetivo es definir hacia dónde vamos.*

- [ ] **Diseño del nuevo SIASE (UI):** Definir paleta de colores, tipografías y el estilo general (ej. glassmorphism, flat design). Crear un boceto simple en Figma/Canva de cómo deberían verse las pantallas clave (Login, Horario, Kardex).
- [ ] **Definición de Variables CSS (Tokens):** Traducir los colores y fuentes decididos por el diseñador a código. Crear las reglas de variables `:root` en `content.css` para que todos usen los mismos colores (ej. `--uanl-blue`, `--uanl-gold`).

## Fase 2: 🏗️ Infraestructura y Estructura
*Preparación técnica para el trabajo en equipo paralelo.*

- [ ] **Configuración en GitHub:** Crear un [Tablero de Proyecto tipo Kanban en GitHub (Projects)](https://github.com/features/issues) con 3 columnas ("Por hacer", "Haciendo", "Terminado") y pasar estas tareas ahí.
- [ ] **Investigación de URLs internas:** Navegar por el SIASE y recolectar las URLs de los iframes internos (ej. las secciones de Kardex, Trámites, Horario) para agregarlas al `manifest.json`.

## Fase 3: 💻 Implementación Frontend y Rediseño CSS
*El "Core" del rediseño. Modificar visualmente la aplicación.*

- [ ] **Login:** Aplicar el estilo moderno a la tabla/formulario de inicio de sesión (iframe `deimos.dgi.uanl.mx`).
- [ ] **Menú Lateral y Header Principal:** Cambiar el color de fondo, estilos de fuentes e iconos del menú de navegación una vez que entras al SIASE.
- [ ] **Tablas de Información:** Rediseñar genéricamente todas las filas y celdas de las tablas (`td`, `tr`) para quitar ese look antiguo de HTML "crudo" por uno minimalista y espaciado.
- [ ] **Página de Horario:** Mejorar el esquema y visualización visual de la cuadrícula de clases (separación, colores de cada clase).

## Fase 4: 🛠️ Funciones Adicionales (JavaScript) 
*Nuevas herramientas que los estudiantes amarán (Mejoras de calidad de vida).*

- [ ] **Promedio Automático en Kardex:** agregar funcion al script (`content.js`) para que al entrar a la página de Kardex, lea la tabla de materias calificadas y coloque tu Promedio Global en número grande hasta arriba.
- [ ] **Exportación visual del Horario:** (Opcional - MVP avanzado) Crear un botón que lea la tabla de tu horario y genere un diseño limpio listo para tomar captura o descargar a imagen para guardar en el dispositivo

## Fase 5: 🐞 Testing (QA) y Ajustes
*Revisión de calidad en equipo.*

- [ ] **QA Multipantalla:** Probar la extensión abriendo el navegador en distintos tamaños (PC, laptop). Buscar y reportar botones ocultos o sobrepuestos.
- [ ] **Manual de Uso MVP:** Subir a GitHub en el README un pequeño video en .gif mostrando el antes/después y los beneficios para atraer a nuevos colaboradores o que los estudiantes quieran probarlo.

---

## 🛠️ Flujo de Trabajo con Git (Ramas)

Para mantener el código organizado y no pisar el trabajo de los demás en la rama principal (`main`), utilizaremos un sistema de **Ramas (Branches)**. 

Cada vez que vayas a empezar una nueva tarea de la lista de arriba, **nunca programes directamente en `main`**. Sigue estos pasos:

1. **Asegúrate de estar actualizado:**
   Abre tu terminal en la carpeta del proyecto y descarga los últimos cambios:
   ```bash
   git checkout main
   git pull origin main
   ```

2. **Crea tu propia rama para la tarea:**
   Nombra tu rama describiendo brevemente lo que harás (ej. `feature/rediseño-login` o `feature/promedio-kardex`):
   ```bash
   git checkout -b feature/nombre-de-tu-tarea
   ```

3. **Programa y haz tus Commits locales:**
   Trabaja normalmente en tu editor. Cuando termines una parte importante guarda tus cambios en esa rama:
   ```bash
   git add .
   git commit -m "Agregado soporte para calcular promedio en Kardex"
   ```

4. **Sube tu rama y pide revisión (Pull Request):**
   Envía tu rama a GitHub:
   ```bash
   git push origin feature/nombre-de-tu-tarea
   ```
   Luego ve a la página del repositorio en GitHub. Verás un botón verde que dice **"Compare & pull request"**. Dale clic, ponle título y avisa en el grupo para que alguien más revise y apruebe tu código antes de que se fusione oficialmente con `main`.
