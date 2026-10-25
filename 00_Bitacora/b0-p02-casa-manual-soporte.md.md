

- **Alumno:** Youcef Bourek Kaid Omar
    
      
    
- **Bloque:** B0 — Prerrequisitos
    
      
    
- **Fase / ejercicio:** Fase 0.1 / P02 Casa Manual de soporte
    
      
    
- **Fecha de inicio:** 25/10/2026
    
      
    
- **Fecha de entrega:** 25/10/2026
    
      
    

## 🎯 Qué se pedía

Crear desde cero un manual técnico de soporte en una bóveda de Obsidian (`Boveda_Manual_Casa`) y versionar solo la carpeta `01_Proyecto` mediante Git. Había que publicar el proyecto en un repositorio de GitHub (`sor-manual-soporte-casa`), registrando el historial a lo largo de tres entregas/versiones, probar la navegación histórica entre commits y finalizar cerrando la bitácora en un cuarto commit documental.

  

## ⌨️ Comandos y pasos importantes

- `git --version` — Muestra la versión instalada de Git.
    
      
    
- `git config --global user.name` / `user.email` — Consulta la identidad configurada del autor.
    
      
    
- `ls -l ~/.ssh/id_ed25519 ~/.ssh/id_ed25519.pub` — Comprueba la presencia de las claves SSH sin revelar su contenido.
    
      
    
- `ssh -T git@github.com` — Valida la autenticación por SSH con GitHub.
    
      
    
- `pwd` — Muestra la ruta completa del directorio de trabajo actual para verificar la ubicación antes de inicializar o realizar operaciones.
    
      
    
- `git init` — Inicializa un repositorio Git local en la carpeta actual (`01_Proyecto`).
    
      
    
- `git branch -M main` — Establece el nombre de la rama principal como `main`.
    
      
    
- `git remote add origin git@github.com:TU-USUARIO/sor-manual-soporte-casa.git` — Asocia el repositorio local con el repositorio remoto de GitHub por SSH.
    
      
    
- `git status` / `git status --short --untracked-files=all` — Consulta el estado de los archivos (nuevos, modificados o preparados).
    
      
    
- `git diff` — Compara las diferencias del directorio de trabajo frente al área de preparación (índice).
    
      
    
- `git diff --cached` / `git diff --cached --stat` — Muestra y resume las modificaciones que están listas en el área de preparación antes del commit.
    
      
    
- `git add <archivo>` — Añade un archivo específico al área de preparación (índice).
    
      
    
- `git commit -m "mensaje"` — Guarda una versión local con una descripción descriptiva.
    
      
    
- `git push -u origin main` / `git push` — Sube las versiones locales guardadas a la rama del repositorio en GitHub.
    
      
    
- `git check-ignore -v <archivo>` — Verifica qué regla de `.gitignore` está excluyendo a un archivo local.
    
      
    
- `git log --oneline` — Muestra un historial simplificado de commits en una sola línea por versión.
    
      
    
- `git switch --detach <CODIGO_COMMIT>` — Desplaza temporalmente los archivos de trabajo a la versión exacta de un commit sin alterar las ramas.
    
      
    
- `git switch main` — Regresa a la rama principal `main` con todo el historial actualizado.
    
      
    

## 🛠️ Qué he hecho

1. **Aislamiento y estructura inicial:** Comprobé la ruta de trabajo local independiente fuera de OneDrive y de cualquier árbol de SOR previo. Creé la estructura de carpetas de la bóveda (`00_Grabaciones`, `01_Proyecto`, `01_Proyecto/00_Bitacora`, `01_Proyecto/manual/procedimientos`).
    
      
    
2. **Archivos iniciales y `.gitignore`:** Creé el archivo `.gitignore` excluyendo formatos multimedia (`*.mp4`, `*.mkv`, etc.), la bitácora inicial, el archivo `README.md` y el primer procedimiento `sin-conexion.md`.
    
      
    
3. **Inicialización y vinculación remota:** Verifiqué la ubicación con `pwd` en `01_Proyecto`, inicialicé Git, renombré la rama a `main`, creé el repositorio en GitHub (`sor-manual-soporte-casa`) y configuré la URL SSH de `origin`.
    
      
    
4. **Primera versión:** Preparé archivo a archivo (`.gitignore`, bitácora, README y procedimiento), verifiqué con `git diff --cached`, creé el commit `"Crear manual inicial de soporte"` y realicé el primer `git push -u origin main`.
    
      
    
5. **Segunda versión:** Reordené los pasos en `sin-conexion.md` (poniendo primero la revisión del cable y después la prueba en navegador), comprobé el `diff`, preparé el archivo, hice commit (`"Corregir comprobacion de conexion del manual"`) y subí los cambios.
    
      
    
6. **Tercera versión (Ampliación):** Añadí los nuevos manuales (`impresora.md` y `sin-sonido.md`), incorporé una imagen PNG (`diagnostico.png`) e incluyo dos vídeos de prueba `.mp4` para comprobar que `.gitignore` los excluía. Preparé individualmente cada recurso del producto, revisé con `diff --cached`, realicé el commit `"Anadir impresora sonido e imagen al manual"` y subí los cambios a GitHub.
    
      
    
7. **Consulta histórica:** Verifiqué estar en `main` sin cambios pendientes, obtuve el hash del primer commit con `git log --oneline`, navegué a él mediante `git switch --detach` para comprobar las diferencias del manual en esa versión inicial y regresé a `main` con `git switch main`.
    
      
    
8. **Cierre documental:** Finalicé la grabación, subí el vídeo a YouTube, añadí las marcas de tiempo reales a la bitácora, realicé un cuarto commit (`"Completar bitacora y enlace del video de casa"`) y lo envié al repositorio en GitHub.
    
      
    

## 🚩 Qué me ha fallado y cómo lo he resuelto

_(Si durante la ejecución real de tu práctica has tenido un error concreto, sustituye esta sección por el mensaje literal y la solución aplicada. De lo contrario:)_

  

**Error/Inconveniente:** Ninguno. Se han seguido de forma exacta todos los pasos de verificación (`git status`, `git diff`, `pwd` y comprobación previa antes de guardar/subir), asegurando que las rutas, identidades y áreas de preparación estuvieran totalmente limpias e independientes antes de ejecutar cada acción.

  

## 🤔 Respuestas a las preguntas

1. **¿Por qué Git se inicializa solo en `01_Proyecto` y la grabación queda fuera?** Porque solo el contenido final del producto (`01_Proyecto`) debe formar parte del repositorio versionado. La grabación y las configuraciones de Obsidian son recursos de trabajo/entrega locales que no pertenecen al historial del código o manual.
    
      
    
2. **¿Qué muestran `status` y `diff` antes de preparar la corrección del procedimiento? Cita la instrucción anterior y la nueva.** `git status` muestra que el archivo `manual/procedimientos/sin-conexion.md` ha sido modificado. `git diff` refleja que se retiró la línea `- 1. Abre el navegador y prueba la página interna.` y se incorporó como primera comprobación `+ 1. Comprueba visualmente que el cable de red está conectado.`.
    
      
    
3. **¿Por qué un archivo nuevo aparece en `status` pero no en el `diff` de `README.md`?** Porque un archivo totalmente nuevo está "sin seguimiento" (_untracked_). `git diff` solo compara los cambios dentro de los archivos que Git ya rastrea o las diferencias registradas entre el disco y el índice para dicho archivo especifico.
    
      
    
4. **¿Qué preparas con cada `add` y qué compruebas con `diff --cached` antes del commit?** Con cada `add` se añade exactamente el contenido actual de un archivo al área de preparación (índice). Con `git diff --cached` se comprueba el contenido exacto y las líneas de texto que van a incluirse definitivamente en el nuevo commit antes de guardarlo.
    
      
    
5. **¿Qué demuestra `check-ignore` y qué comprobaste además para saber que los clips existen?** Demuestra que la regla activa en `.gitignore` (como `*.mp4`) detecta los archivos e impide que Git los rastree por accidente. Además, se comprobó en el gestor de archivos que los clips continuaban en el disco y se reprodujeron localmente.
    
      
    
6. **¿Qué diferencias concretas observaste en el manual del primer commit y qué recuperaste al volver a `main`?** En el primer commit, la comprobación del navegador figuraba en primer lugar, y no existían los manuales de impresora o sonido, ni la imagen `diagnostico.png`. Al volver a `main`, se recuperó la versión corregida (cable en primer lugar) y los tres enlaces junto a la captura del diagrama.
    
      
    
7. **¿Qué aporta un historial cuando dos técnicos necesitan conocer el procedimiento vigente?** Permite auditar las instrucciones vigentes en cada momento del tiempo, comparar cambios pasados y entender la evolución del manual sin riesgo de perder versiones anteriores o solapar modificaciones.
    
      
    
8. **¿Por qué `commit` y `push` son acciones diferentes y qué miraste en GitHub?** `commit` es una acción local que guarda la instantánea en la base de datos de Git del equipo; `push` transfiere esos commits locales al repositorio remoto en GitHub. En GitHub se comprobó que los archivos, enlaces, e imágenes aparecieran actualizados y que no figurara ningún archivo o recurso ignorado.
    
      
    
9. **¿Qué pasos repetirías para corregir otra instrucción y cuáles se hicieron una sola vez?**
    
      
    - **Se repiten:** Editar el archivo, comprobar `status`/`diff`, preparar con `git add`, hacer `commit` con mensaje y subir con `git push`.
        
          
        
    - **Se hacen una sola vez:** Crear las carpetas iniciales, ejecutar `git init`, renombrar la rama a `main` y vincular el servidor remoto con `git remote add origin`.
        
          
        

## 🔗 Enlaces


## 💭 Dudas / a repasar

