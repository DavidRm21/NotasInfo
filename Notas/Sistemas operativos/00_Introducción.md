###### Mis notas obtenidas en el libro "Fundamentos de Sistemas Operativos, 7ma Edición, Silberschatz Galvin Gagne"

# ¿Qué hace un sistema operativo?

Primeramente, analizamos la función de un sistema operativo en un entorno informático integral.

![Entorno informatico](./img/EntornoInformatico.jpg)

Un sistema informático puede dividirse en cuatro componentes:

- El hardware, la unidad de procesamiento, la memoria y los dispositivos de E/S, proporcionan los recursos básicos de cómputo al sistema. (Hardware, software y datos) 

- Los programas de aplicación, como los procesadores de texto, las hojas de cálculo, los compiladores y los exploradores web, definen las formas en que estos recursos se emplean para resolver los problemas informáticos de los usuarios. 

El sistema operativo controla y coordina el uso del hardware entre los diversos programas de aplicación por parte de los distintos usuarios.

El sistema proporciona los medios para hacer un uso adecuado de estos recursos durante el funcionamiento del sistema



## Sistema visto desde el usuario

La perspectiva del usuario es diversa de acuerdo a la interfaz que utilice. 

- La mayoría usa monitor, teclado, ratón y una unidad de sistema, un sistema así se diseña para que el usuario pueda monopolizar sus recursos.

    ![](https://img.freepik.com/vector-gratis/ilustracion-concepto-computo-escritorio-moderno_114360-12156.jpg?w=2000)

    - Maximizar el trabajo que el usuario realice. 

    - El sistema operativo está diseñado principalmente para que sea de fácil uso.

    - Presta cierta atención al rendimiento y ninguna a la utilización de recursos

    <br>
    <br>

- Mainframe o una microcomputadora:
    
    ![P2P](https://cdn.goconqr.com/uploads/image_clipping/image/157045/Primeras_redes.JPG)

    Otros usuarios pueden acceder simultáneamente desde otros terminales, estos usuarios comparten recursos e información. 

    - El sistema opereativo está diseñado para maximizar la utilización de recursos-

    - El CPU, la memoria y E/S disponibles se usan de forma equitativa en todo el sistema.

    <br>
    <br>

- Estaciones de trabajo conectadas a otras y servidores. 

    ![WorkStation](https://bighardware.es/wp-content/uploads/2021/08/Que-es-una-Red-Informatica.webp)

    - Estos usuarios tienen recursos dedicados a su disposición.

    - Tambien tienen recursos compartidos como la red y los servidores (servidores de archivos, calculo, impresion, etc)

    <br>
    <br>

> Por tanto, su sistema operativo está diseñado para llegar a un compromiso entre la usabilidad individual y la utilización de recursos.

Tambien existen computadoras que tienen poca o ninguna interacción con los usuarios. Por ejemplo, en algunos electrodomesticos y en los automoviles, disponen de teclados numericos e indicadores luminosos para representar algún estado, los sistemas operativos estan diseñados para que no necesite intervención del usuario.

![Computadora auto](https://www.nitro.pe/images/2016/diciembre/compu_carro.jpg)

<br>

## Sistema visto desde el sistema

El sistema operativo es el programa más intimmamente relacionado con el hardware. 

![Sistema operativo](https://www.lifeder.com/wp-content/uploads/2018/02/sistema-ordenador-min.jpg)

- Puede ser visto como un asignador de recursos. 

- Se enfrenta a numeros y posibles solicitudes conflictivas de recursos.

- Se encarga de que la computadora opere de manera eficiente y equitativa.

- Un sistema operativo es como un programa de control, gestiona la ejecución de los programas de usuario para evitar errores y mejorar el uso de la computadora.

- Funcionamiento y control de los dispositivos E/S.

<br>

## Definición del sistema operativo

Es aquel programa que se ejecuta continuamente en una computadora, es critico para el rendimiento y la estabilidad del sistema. 

Es aquel que gestiona los recursos de hardware y permite que las aplicaciones y los procesos se comuniquen con el hardware de la computadora. El kernel actúa como una capa de abstracción entre el hardware y el software, facilitando la interacción.

<br>
<br>

## Organización de una computadora

<br>

### Funcion de una computadora

Una computadora moderna de proposito general consta de una o mas CPU y de una serie de controladores de dispositivo conectadas atraves de un bus común que proporciona acceso a una memoria compartida.

Cada controladora de dispositivo se encarga de un tipo especifico de dispositivo (discos, audio, pantalla de video, etc)

Para asegurar el acceso de forma ordenada a la memoria compartida se proporciona una controladora de memoria cuya función es sincronizar el acceso a la misma.

Para que una computadora comience a funcionar debe existir un programa de inicio. Normalmente se almacena en una memoria ROM o EEPROM y se conoce generalmente como ***firmware***, dentro del hardware de la computadora.

El programa de arranque debe saber como cargar el sistema operativo e iniciar la ejecución de dicho sistema. Para conseguirlo el programa localiza y carga en memoria el kernel del sistema operativo. Despues comienza ejecutando el primer proceso y espera a que se produzca algun suceso.

![](https://sistemasoperativos502027821.files.wordpress.com/2018/08/software.gif)

La ocurrencia de un suceso normalmente se indica mediante una interrupción bien sea del hardware o bien del software. El hardware puede activar una interrupción en cualquier instante enviando una señal a la CPU, normalmente a través del bus del sistema. El software puede activar una interrupción ejecutando una operación especial denominada llamada del sistema(System call)

Cuando se interrumpe a la CPU, deja lo que esta haciendo e inmediatamente transfiere la ejecución a una posición establecida, el sistema implica el uso de una tabla de punteros, que se almacena en la memoria generalmente en las primeras 100 posiciones. Cada posición almacena la dirección de la rutina de servicio correspondiente para un dispositivo específico. Cuando se genera una interrupción, se utiliza un número de dispositivo único para indexar la tabla de punteros y obtener la dirección de la rutina de servicio adecuada. 
Si la rutina de interrupción necesita modificar el estado del procesador, como los valores de los registros, debe guardar y luego restaurar explícitamente el estado actual antes de continuar. Después de manejar la interrupción, la dirección de retorno guardada se carga en el contador de programa, y el cálculo interrumpido se reanuda como si la interrupción no hubiera ocurrido.

![](./img/eventos.jpg)