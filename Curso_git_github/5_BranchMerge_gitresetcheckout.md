![BranchMerge](https://static.platzi.com/media/user_upload/ramas-branch-en-git-7e72b407-90cc-4b90-8de1-738b155764eb.jpg)

¿Qué es branch y un Merge en git?

Una rama (Branch) te permite trabajar en diferentes partes de tu proyecto sin afectar el código principal. Y un Merge te ayuda a combinar los cambios de esas ramas de manera ordenada en tu código principal, manteniendo todo organizado y sin conflictos si es posible.

*Si hay partes del código principal que se modificaron en ambas ramas, puede haber conflictos. *

![Flujo de trabajo normal en git](https://static.platzi.com/media/user_upload/GIT_Branch-6809996b-6dec-48d7-9469-1412f337c25d.jpg)


# Git reset 

El comando "git checkout" junto con el ID del commit nos permite viajar en el tiempo en Git. Puedes regresar a versiones anteriores de archivos específicos o incluso del proyecto completo. También se usa para crear ramas y moverse entre ellas.

```terminal
git checkout codigoCommit nombreArchivo

git checkout main nombreArchivo
```

Otra forma de hacer esto es mediante el comando "git reset". Aquí, no solo retrocedes en el tiempo, sino que también deshaces los cambios realizados después de un commit.

Existen dos formas de utilizar "git reset":

- Con --hard, eliminas toda la información en el área de preparación (staging), perdiendo esos cambios. (Suele utilizarse)

```terminal
git reset codigoDelCommit --hard
```

- Con --soft, más seguro, mantienes los cambios en el área de preparación para aplicarlos desde un commit anterior.

```terminal
git reset codigoDelCommit --soft
```

![git rm y git reset](https://static.platzi.com/media/user_upload/git-reset%20%281%29-77a1294a-fb8b-43d0-aace-a517c1a05c2e.jpg)

En resumen:

- "git checkout" y "git reset" permiten regresar en el tiempo en Git.
- "git reset" ofrece opciones como --soft, --mixed y --hard para controlar cómo reviertes cambios.
- "git reset --soft [SHA 1]" elimina cambios hasta el área de preparación.
- "git reset --mixed [SHA 1]" elimina cambios hasta el directorio de trabajo.
- "git reset --hard [SHA 1]" regresa al commit con el identificador [SHA-1].

![ciclo de vida git](./gitLocalRemoteJPG.jpg)
