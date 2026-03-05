# Git Guide – Video Player Project

## 1. Comandos más usados

### Inicializar repositorio

git init

### Ver estado del repositorio

git status

### Añadir archivos

git add .

### Crear commit

git commit -m "mensaje descriptivo del cambio"

### Ver historial de commits

git log

### Crear una nueva rama

git checkout -b nombre-rama

### Cambiar de rama

git checkout nombre-rama

### Subir cambios al repositorio remoto

git push origin nombre-rama

### Descargar cambios del repositorio remoto

git pull origin main

---

# 2. Flujo de trabajo recomendado

1. Clonar el repositorio

git clone https://github.com/usuario/video-player-practice.git

2. Crear una rama para una nueva funcionalidad

git checkout -b feature-video-controls

3. Realizar cambios en el código (HTML o CSS)

4. Revisar cambios

git status

5. Añadir cambios

git add .

6. Crear commit

git commit -m "Improve styling of video player controls"

7. Subir la rama

git push origin feature-video-controls

8. Crear Pull Request en GitHub

9. Revisar cambios y hacer merge en main

---

# 3. Resolución de conflictos

Un conflicto ocurre cuando dos ramas modifican la misma línea de un archivo.

Ejemplo de conflicto en un archivo CSS:

<<<<<<< HEAD
color: red;
===========

color: blue;

> > > > > > > main

Para resolverlo:

1. Abrir el archivo con conflicto.
2. Elegir qué cambio mantener o combinar ambos.
3. Eliminar los marcadores de conflicto.
4. Guardar el archivo.

Después ejecutar:

git add .
git commit -m "Resolve merge conflict in style.css"

Esto completa la resolución del conflicto.

---

# 4. Errores comunes

### 1. Olvidar hacer git add

Si haces commit sin añadir archivos primero:

git commit -m "update css"

Git mostrará:
nothing to commit

Solución:

git add .

---

### 2. Subir archivos innecesarios

Ejemplo:

* node_modules
* archivos temporales
* archivos del sistema

Solución: usar `.gitignore`

---

### 3. Trabajar directamente en main

Modificar directamente la rama principal puede causar problemas.

Solución:
Siempre crear una rama de trabajo:

git checkout -b feature-new-ui

---

### 4. Mensajes de commit poco claros

Mal ejemplo:

update

Buen ejemplo:

Improve video player layout and button styling

---

# 5. Buenas prácticas

### 1. Usar commits pequeños y claros

Cada commit debe representar un cambio específico.

Ejemplo:

Add basic HTML structure for video player

---

### 2. Escribir mensajes de commit descriptivos

Un buen mensaje explica qué cambio se realizó.

Ejemplo:

Fix CSS alignment issue in video controls

---

### 3. Usar ramas para nuevas funcionalidades

Nunca desarrollar directamente en main.

Ejemplo de ramas:

feature-controls
feature-style-update
bugfix-player-size

---

### 4. Revisar cambios antes de hacer commit

git status
git diff

Esto ayuda a evitar errores.

---

### 5. Mantener el repositorio limpio

Usar `.gitignore` para evitar subir:

* archivos temporales
* configuraciones locales
* credenciales o secretos

Nunca subir contraseñas o claves API al repositorio.

---

# 6. Lecciones aprendidas

Durante esta práctica se aprendió:

* Cómo inicializar un repositorio con Git
* Cómo realizar commits correctamente
* Cómo trabajar con ramas
* Cómo crear Pull Requests en GitHub
* Cómo resolver conflictos de integración
* Importancia de mantener buenas prácticas en repositorios
