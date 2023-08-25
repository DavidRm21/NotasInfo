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

Otros comandos que podemos encontrar son:

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
    ```

- Elimina un archivo del área de preparación. Para borrarlo por completo, usar git rm --cached.

    ```terminal
    git rm <nombreArchivo>
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

## Analizar cambios en los archivos del proyecto de git

![git diff](https://static.platzi.com/media/user_upload/Analizar%20cambios%20en%20los%20archivos%20de%20tu%20proyecto%20con%20Git-f6f2fe08-e2e9-46ef-86fa-6180354bc151.jpg)

1. 