### GIT BASICO
Guia ampliada y complementaria basada en "Pro GIT"

## 1. ¿Que es GIT?
1. Git como software
* Git es un sistema de control de versiones distribuido que instalas en tu máquina. Funciona desde la terminal (Git Bash, Terminal nativo, o la terminal integrada de VSCode).
* Internamente, Git guarda tu proyecto en un directorio oculto .git/ con un modelo de objetos basado en SHA-1.

2.¿Para qué sirve?
* Mantener un historial completo de cambios.
* Facilitar la colaboración y ramas independientes.
*Permitir volver a versiones anteriores sin perder trabajo.

3.Analogía
* Como una máquina del tiempo para tu código: cada commit es una fotografía que puedes revisar o restaurar.

2. Modelo de datos interno (según Pro Git)
3. 
Git distribuye la gestión de tu proyecto en tres áreas distintas. Entenderlas te ayuda a visualizar qué hace Git en cada paso:
Directorio de trabajo (Working Directory)
Aquí ves y editas tus archivos (por ejemplo, index.html, app.js, README.md).
Es el “espacio físico” donde trabajas día a día.

Ejemplo: abres main.css, cambias un color y guardas; ese cambio ocurre solo en el directorio de trabajo.

Área de preparación (Staging Area o Index)
Es una zona intermedia donde seleccionas cambios para el siguiente commit.
Cuando ejecutas git add archivo.txt, le dices a Git: “Quiero incluir este cambio en mi próxima fotografía”.
Analogía: imagina una bandeja donde pones documentos antes de imprimirlos; solo los que estén en la bandeja se imprimen.

Repositorio (.git/ directory)
Carpeta oculta donde Git guarda el historial completo (objetos y referencias).
Aquí no tocas nada directamente: es el “almacén seguro” de todas tus versiones.

2.1. Objetos fundamentales
Git usa tres tipos de objetos para representar tu proyecto:
Blob (Binary Large OBject)
Guarda el contenido exacto de un solo archivo, sin nombre ni ruta.
Se identifica con un hash SHA-1 (una cadena de 40 caracteres).
Ejemplo: si README.md vale “Hola mundo”, Git crea un blob con ese texto.

Tree
Actúa como directorio: apunta a blobs (archivos) y a otros trees (subcarpetas).
Almacena nombres, permisos y hashes de los blobs/trees.
Ejemplo: un tree para la carpeta src/ que contiene app.js y otro tree para components/.
