## Analizar cambios en los archivos del proyecto de git

![git diff](https://static.platzi.com/media/user_upload/Analizar%20cambios%20en%20los%20archivos%20de%20tu%20proyecto%20con%20Git-f6f2fe08-e2e9-46ef-86fa-6180354bc151.jpg)

1. Exploramos los commits y mensajes más recientes que registran cambios en el archivo

```terminal
git log nombreArchivo
```

2. Examinamos los cambios que han ocurrido en un archivo específico.

```
git show nombreArchivo
```

Git show es una herramienta valiosa, cuando se trata de depurar problemas en el código. Te permite examinar los cambios anteriores y entender cómo evolucionó el código con el tiempo. Esto es fundamental para identificar por qué algo que funcionaba previamente ahora está roto y cómo se puede solucionar. 

3. Para obtener claridad sobre las variaciones entre diferentes versiones y para identificar qué líneas de código han sufrido modificaciones, agregados o eliminaciones, puedes utilizar el comando "git diff". Una vez hayas copiado el número de commit que se muestra al usar "git show", ejecuta "git diff" junto con ese identificador. Esto te permitirá visualizar de manera detallada los cambios específicos que ocurrieron en el archivo entre el commit previo y el commit seleccionado.

```terminal
git log nombreArchivo
```

![Numero del commit](https://static.platzi.com/media/user_upload/Screenshot_1-93e2142f-fc7d-414d-a85b-6cb4e41e0b72.jpg)

```terminal
git diff cambioReciente cambioAnterior
```

![Diferencia entre cambios](https://static.platzi.com/media/user_upload/Screenshot_2-2cc23836-5299-4dd3-8f63-3bc77476a647.jpg)