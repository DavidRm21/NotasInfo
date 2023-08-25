## ¿Cómo iniciar git?

1. Inicia un nuevo repositorio Git en la carpeta actual.

    ```terminal
    git init
    ```

2. Agrega archivos al área de preparación para el próximo commit.

    ```terminal
    git add <nombreArchivo>
    ```

- Muestra el estado actual del repositorio, incluyendo archivos añadidos o borrados, la rama actual y los commits pendientes.

    ```terminal
    git status
    ```

3. Crea un nuevo commit con los archivos en el área de preparación y un mensaje descriptivo.

    ```terminal
    git commit -m 'mensajeDelCambio'
    ```

## Configuración de git con nuestros datos

- Muestra o configura ajustes de Git.

    ```terminal
    git config --list
    ```

- Muestra donde se guardan los ajustes de Git. (Avanzado)

    ```terminal
    git config --list --show-origin
    ```

- Cambio del nombre de usuario globalmente.

    ```terminal
    git config --global user.name "nombreDeUsuario"
    ```

- Cambio del correo del usuario globalmente.

    ```terminal
    git config --global user.email "correo@mail.com"
    ```

<hr>

## Otros comandos que podemos encontrar son:

- Agrega todos los archivos modificados y nuevos en el directorio de trabajo al área de preparación para el próximo commit. *Es importante los espacios*

    ```terminal
    git add .
    ```

- Muestra información detallada sobre un commit específico, incluyendo cambios, autor, fecha y mensaje.

    ```terminal
    git show
    ```

- Muestra el historial de commits, cambios y detalles de autoría.

    ```terminal
    git log <archivo>

    git log --stat
    ```

- Elimina un archivo del área de preparación. Para borrarlo por completo, usar git rm --cached.

    ```terminal
    git rm <nombreArchivo>
    ```

- git checkout: Cambia entre versiones anteriores.

- git diff: Muestra diferencias entre versiones.

- git reset --hard: Revierte a una versión anterior y elimina cambios.

- git reset --soft: Revierte a una versión anterior sin eliminar cambios.

- git rm --cached: Elimina archivo del área de preparación pero no del disco.

- git clone: Clona un repositorio remoto en local.

- git push: Envía cambios locales al repositorio remoto.

- git fetch: Trae cambios remotos sin mezclar.

- git merge: Combina cambios en local.

- git pull: Trae y mezcla cambios remotos en local.

- git commit -a: Crea commit directamente en master sin pasar por el staging.

- git branch: Muestra o crea ramas.

- git tag: Crea y muestra versiones.

- git remote: Configura repositorios remotos.

- git stash: Guarda temporalmente cambios.

- git clean: Borra archivos no deseados.

- git cherry-pick: Trae un commit de otra rama.

- git reflog: Muestra registro de acciones.

- git grep: Busca palabras o archivos.

- git blame: Muestra cambios y autores de línea.

- git shortlog: Resumen de commits por autor.

- git rebase: Cambia la base de commits (evitar en remoto).

- Keygen ssh: Crea claves seguras para SSH.

- Alias: Crea atajos para comandos.

