# SIASE Mejorado 🎓

**SIASE Mejorado** es una extensión de navegador (Chrome/Edge) diseñada para modernizar la interfaz del sistema SIASE de la UANL y en un futuro agregar funciones útiles que faciliten la vida de los alumnos. El objetivo principal es renovar la estética visual (actualmente anticuada) y optimizar el flujo de trabajo de los estudiantes al interactuar con el portal de servicios en línea.

## 📋 Tareas
Para estar al tanto de la tareas actuales para el proyecto visita el documento [TASKS.md](https://github.com/Julian-ops-vital/Extension-Siase/blob/main/TASKS.md)

## 👥 Para Colaboradores

Si deseas sumarte a mejorar este proyecto, puedes clonar o conectar el repositorio a tu propio equipo siguiendo estos pasos:

### 1. Clonar el repositorio
Abre tu terminal y ejecuta el siguiente comando en la carpeta que elijas para tus proyectos:
```bash
git clone https://github.com/Julian-ops-vital/Extension-Siase.git
```



### 2. Cómo testearlo localmente para programar
Como esta pequeña arquitectura es una "Extensión de Navegador", no necesitas Node.js, `npm run dev` ni ningún servidor para ver los cambios. En su lugar, instalas la extensión "sin empaquetar" (unpacked):

1. Abre Google Chrome (o tu navegador basado en Chromium como Edge/Brave).
2. En la barra de direcciones visita `chrome://extensions/`.
3. Arriba a la derecha, **activa el interruptor de "Modo desarrollador" (Developer mode)**.
4. Aparecerá un botón arriba a la izquierda que dice **"Cargar descomprimida" (Load unpacked)**. Selecciónalo.
5. Selecciona la carpeta de este repositorio (la que contiene el archivo `manifest.json`).

### 3. ¡Desarrollar y ver los cambios! 🚀
Con la extensión cargada, entra a [https://www.uanl.mx/enlinea/](https://www.uanl.mx/enlinea/).  
Cada vez que realices algún cambio en el código (ya sea arreglando el HTML, CSS o los archivos JavaScript) tienes que:
1. **Guardar** los archivos en tu editor de código.
2. Ir a la pestaña `chrome://extensions/`.
3. Buscar la tarjeta de "SIASE Mejorado" y presionar el botón con la **flecha curva para recargar** la extensión.
4. Actualizar (F5) la página del SIASE para ver tu código en funcionamiento.

---
*¡Todo tipo de modificaciones y "Pull Requests" (solicitudes de cambios) son bienvenidas!*
