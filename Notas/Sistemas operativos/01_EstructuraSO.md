
# Estructuras de los sistemas operativos

El sistema operativo es una parte fundamental de cualquier computadora y proporciona el entorno en el que se ejecutan los programas. Su diseño y composición varían significativamente, y su desarrollo es una tarea compleja que requiere una clara definición de objetivos. 

- **Diversidad de Sistemas Operativos:** Los sistemas operativos pueden variar en su composición y diseño. La elección de un enfoque específico depende de los objetivos y requisitos del sistema.

- **Definición de Objetivos:** Antes de diseñar un sistema operativo, es crucial definir claramente sus objetivos. Estos objetivos servirán como guía para tomar decisiones sobre algoritmos y estrategias.

- **Vistas del Sistema Operativo:** Se pueden abordar los sistemas operativos desde diferentes perspectivas, como los servicios que proporcionan a los usuarios, la interfaz que ofrecen a los programadores y su estructura interna.

- **Servicios del Sistema Operativo:** Los sistemas operativos ofrecen una variedad de servicios, como la gestión de recursos de hardware, la administración de procesos y la comunicación entre programas.

- **Interfaz para Usuarios y Programadores:** El sistema operativo proporciona una interfaz que permite a los usuarios interactuar con la computadora y a los programadores desarrollar aplicaciones. Estas interfaces varían según el sistema operativo.

- **Diseño y Metodologías:** Se exploran diferentes enfoques y metodologías utilizadas en el diseño de sistemas operativos, destacando la importancia de la planificación cuidadosa.

- **Creación e Inicio del Sistema Operativo:** Se describe cómo se crea un sistema operativo y cómo una computadora inicia su sistema operativo cuando se enciende.

<br>
<br>

# Servicios del sistema operativo

### Servicios para Usuarios:

- **Interfaz de Usuario:** Los sistemas operativos proporcionan interfaces de usuario, como la línea de comandos (CLI) o la interfaz gráfica de usuario (GUI), para interactuar con la computadora.

- **Ejecución de Programas:** El sistema carga y ejecuta programas, asegurando que puedan finalizar tanto de forma normal como anormal.

- **Operaciones de E/S:** Los programas pueden realizar operaciones de entrada/salida (E/S) hacia archivos y dispositivos. El sistema operativo gestiona estas operaciones.

- **Manipulación del Sistema de Archivos:** El sistema operativo administra archivos y directorios, permitiendo crear, leer, escribir, buscar y gestionar permisos de acceso.

- **Comunicaciones:** Facilita la comunicación entre procesos en la misma computadora o en computadoras conectadas a través de redes, utilizando memoria compartida o paso de mensajes.

- **Detección de Errores:** El sistema operativo detecta y maneja errores en hardware, dispositivos de E/S y programas de usuario, garantizando el funcionamiento correcto y coherente.


### Servicios para la Eficiencia del Sistema:

- **Asignación de Recursos:** Administra la asignación de recursos a usuarios y programas, como ciclos de CPU, memoria, dispositivos de E/S, y realiza planificación de CPU.

- **Responsabilidad:** Realiza un seguimiento del uso de recursos por parte de los usuarios para propósitos contables y estadísticas de uso, lo que puede ayudar en la mejora de los servicios informáticos.

- **Protección y Seguridad:** Controla el acceso a recursos del sistema y garantiza la seguridad frente a intrusiones, autenticando a usuarios y protegiendo dispositivos de E/S.


# Interfaz de Usuario:

Los usuarios interactúan con el sistema operativo principalmente a través de dos métodos: una interfaz de línea de comandos (intérprete de comandos) o una interfaz gráfica de usuario (GUI).

### Intérprete de Comandos:

- Algunos sistemas operativos incorporan el intérprete de comandos en el kernel, mientras que otros lo tratan como un programa especial.

- Los intérpretes de comandos pueden ser seleccionados por los usuarios y se conocen como "shells".

- Su función principal es obtener y ejecutar comandos ingresados por los usuarios, a menudo relacionados con la manipulación de archivos.
- Los comandos pueden ser implementados de dos formas: directamente en el intérprete de comandos o como programas independientes que el intérprete de comandos invoca.

### Interfaces Gráficas de Usuario (GUI):

- Las GUI permiten a los usuarios interactuar con el sistema operativo mediante ventanas, iconos y menús controlados por el ratón.

- Estas interfaces proporcionan una experiencia visual y amigable para realizar tareas y ejecutar programas.

- Ejemplos de GUI incluyen el entorno de escritorio Aqua en Mac OS X y el entorno Windows en Microsoft Windows.

## Elección de Interfaz:

- La elección entre una interfaz de línea de comandos o GUI suele ser una cuestión de preferencia personal.

- Algunos usuarios prefieren la eficiencia de las interfaces de línea de comandos, mientras que otros optan por la comodidad de las GUI.

- Algunos sistemas, como Mac OS X, ofrecen ambas opciones para adaptarse a las preferencias de los usuarios.

### Independencia de la Interfaz de Usuario:

- La interfaz de usuario se separa de la estructura interna del sistema operativo, lo que permite variaciones en la interfaz sin afectar al funcionamiento del sistema.

## Llamadas del sistema

- Las llamadas al sistema proporcionan una interfaz para invocar servicios ofrecidos por el sistema operativo.

- Estas llamadas se implementan generalmente como rutinas en lenguajes como C y C++, aunque tareas de bajo nivel pueden requerir lenguaje ensamblador.

Ejemplo: Creación de un programa para copiar datos de un archivo a otro, lo que involucra múltiples llamadas al sistema.

### Interacción de Usuario y Llamadas al Sistema:

- La interacción de un programa con el usuario a través de un sistema operativo implica secuencias de llamadas al sistema.

Ejemplo: Obtener nombres de archivos de entrada y salida mediante entrada de usuario, abrir archivos, manejar condiciones de error, leer y escribir datos, cerrar archivos y finalizar el programa.

### Uso de API (Interfaz de Programación de Aplicaciones):

- Los programadores de aplicaciones a menudo utilizan una API en lugar de invocar directamente llamadas al sistema.

- Las API especifican un conjunto de funciones y parámetros para interactuar con el sistema operativo.

Ejemplos de API incluyen Win32 para sistemas Windows, POSIX para sistemas basados en UNIX/Linux y la API Java.

### Función de la API y Llamadas al Sistema:

- Las funciones de una API suelen invocar las llamadas al sistema en nombre del programador de aplicaciones.

- La API actúa como un intermediario que oculta la complejidad de las llamadas al sistema al programador.

- La correlación entre funciones de la API y llamadas al sistema se mantiene en la mayoría de los casos.

### Interfaz de Llamadas al Sistema y Biblioteca de Soporte en Tiempo de Ejecución:

- La interfaz de llamadas al sistema intercepta las llamadas de API y mapea las funciones a las llamadas al sistema correspondientes.

- Se utiliza una tabla indexada por números para gestionar las llamadas al sistema.

- La biblioteca de soporte en tiempo de ejecución facilita la gestión de llamadas al sistema y oculta detalles de implementación.

### Pasaje de Parámetros:

- Los parámetros se pasan al sistema operativo de diversas formas, según el sistema y la llamada específica.

- Métodos comunes incluyen el uso de registros, almacenamiento en bloques o tablas en memoria y colocación en la pila.

- El método utilizado depende de la cantidad y longitud de los parámetros.


## Tipos de llamadas del sistema

Las llamadas al sistema se pueden agrupar en cinco categorías principales: control de procesos, manipulación de archivos, manipulación de dispositivos, mantenimiento de información y comunicaciones. 

### Control de procesos

Las llamadas al sistema permiten interrumpir la ejecución de un programa, ya sea de forma normal end() o anormal abort(). Esto puede ocurrir cuando se desea finalizar un programa en ejecución de manera anormal o cuando se produce una excepción de error que resulta en un volcado de memoria o un mensaje de error.

- terminar, abortar
- cargar, ejecutar
- crear procesos, terminar procesos
- obtener atributos del proceso, definir atributos del proceso
- esperar para obtener tiempo
- esperar suceso, señalizar suceso
- asignar y liberar memoria

**Volcado de información en caso de errores:** Cuando ocurren errores en un programa, se puede escribir información de volcado en disco para su posterior análisis por parte de un depurador. Esto ayuda a determinar la causa del problema.

**Retorno al intérprete de comandos:** Después de un error o la finalización de un programa, el sistema operativo debe devolver el control al intérprete de comandos que inició el programa. En sistemas interactivos, el intérprete continúa con el siguiente comando, mientras que en sistemas GUI, se notifica al usuario del error. En sistemas de procesamiento por lotes, se pasa al siguiente trabajo.

**Control de procesos y creación:** Los sistemas operativos permiten la creación y control de procesos. Esto incluye cargar y ejecutar programas, gestionar la terminación de procesos y establecer atributos como prioridad y tiempo máximo de ejecución.

**Espera y coordinación de procesos:** Los sistemas ofrecen llamadas al sistema para esperar a que ocurran eventos específicos o para esperar un período de tiempo determinado. Los procesos pueden señalar eventos cuando se producen.

**Depuración de programas:** Los sistemas proporcionan herramientas para depurar programas, como volcado de memoria, trazado de ejecución e información de perfil de tiempo.

### Administración de archivos

- crear archivos, borrar archivos
- abrir, cerrar
- leer, escribir, reposicionar
- obtener atributos de archivo, definir atributos de archivo

**Creación y eliminación de archivos:** Se requieren llamadas al sistema para crear y eliminar archivos, proporcionando el nombre del archivo y posiblemente algunos atributos.

**Apertura y cierre de archivos:** Es necesario abrir archivos para su uso y cerrarlos cuando ya no se necesitan.

**Lectura y escritura de archivos:** Las llamadas al sistema permiten leer y escribir datos en archivos, así como reposicionarse dentro de ellos.

**Operaciones con directorios:** Si se utiliza una estructura de directorios para organizar archivos, se deben realizar operaciones similares en directorios, como crear, eliminar y abrir.

**Gestión de atributos de archivos:** Se pueden obtener y cambiar atributos de archivos, como nombre, tipo, permisos, información de cuentas de usuario, etc.

**Otras operaciones adicionales:** Algunos sistemas operativos ofrecen más llamadas al sistema para tareas como mover y copiar archivos, o proporcionan APIs y programas del sistema para realizar estas tareas.

### Administración de dispositivos

- solicitar dispositivo, liberar dispositivo
- leer, escribir, reposicionar
- obtener atributos de dispositivo, definir atributos de dispositivo
- conectar y desconectar dispositivos lógicamente

Un proceso en un sistema operativo puede requerir varios recursos para su ejecución, como memoria principal, unidades de disco y acceso a archivos. Si estos recursos están disponibles, se pueden asignar al proceso y este puede continuar su ejecución. En caso contrario, el proceso debe esperar hasta que los recursos necesarios estén disponibles.

Estos recursos se pueden considerar como dispositivos controlados por el sistema operativo, algunos de los cuales son físicos (como cintas) y otros virtuales o abstractos (como archivos). Si varios usuarios están utilizando el sistema, es posible que deban solicitar y liberar el acceso exclusivo a estos dispositivos, similar a las operaciones de abrir y cerrar archivos.

La gestión de dispositivos y archivos en sistemas operativos puede ser muy similar, e incluso algunos sistemas combinan ambos conceptos en una estructura de archivo-dispositivo. La interfaz de usuario también puede hacer que archivos y dispositivos parezcan similares, incluso si las llamadas al sistema subyacentes son diferentes. Esto destaca la importancia de las decisiones de diseño en la creación de sistemas operativos y sus interfaces de usuario.

### Mantenimiento de información

- obtener la hora o la fecha, definir la hora o la fecha
- obtener datos del sistema, establecer datos del sistema
- obtener los atributos de procesos, archivos o dispositivos
- establecer los atributos de procesos, archivos o dispositivos

Muchas llamadas al sistema tienen el propósito de transferir información entre el programa de usuario y el sistema operativo. Esto incluye llamadas para obtener la hora y la fecha actuales, así como para acceder a información sobre el sistema, como el número de usuarios, la versión del sistema operativo, la cantidad de memoria disponible y el espacio en disco.

Además, el sistema operativo mantiene información detallada sobre todos sus procesos, y se utilizan llamadas al sistema para acceder a esta información y configurar los atributos de los procesos, como obtener y establecer atributos del proceso. 

### Comunicaciones

- crear, eliminar conexiones de comunicación 
- enviar, recibir mensajes
- transferir información de estado
- conectar y desconectar dispositivos remotos

existen dos modelos comunes de comunicación interprocesos: el modelo de paso de mensajes y el modelo de memoria compartida.

En el **modelo de paso de mensajes**, los procesos se comunican intercambiando mensajes entre sí, ya sea directamente o a través de un buzón de correo común. Para que la comunicación ocurra, se debe establecer una conexión previa, donde los procesos tienen identificadores que el sistema operativo utiliza para referirse a ellos. Por lo general, el proceso receptor debe aceptar la conexión. Este modelo es adecuado para intercambiar pequeñas cantidades de datos y es relativamente fácil de implementar.

En el **modelo de memoria compartida**, los procesos utilizan llamadas al sistema para obtener acceso a regiones de memoria que son propiedad de otros procesos. Esto requiere que los procesos acuerden compartir información y respetar la sincronización para evitar conflictos. La memoria compartida permite una comunicación más rápida y eficiente, pero plantea desafíos de protección y sincronización entre los procesos que comparten la memoria.

La mayoría de los sistemas operativos implementan ambos modelos, y la elección entre ellos depende de las necesidades específicas de comunicación interprocesos. El modelo de paso de mensajes es útil para pequeñas cantidades de datos y es más fácil de implementar, mientras que la memoria compartida ofrece una comunicación más rápida pero requiere una mayor gestión y precaución en la sincronización.

## Programas del sistema

Son una parte fundamental de los sistemas operativos modernos y desempeñan un papel crucial en la gestión y el funcionamiento de la computadora. Estos programas pueden dividirse en varias categorías:

**Administración de archivos:** Estos programas permiten la creación, eliminación, copia, cambio de nombre, impresión y manipulación general de archivos y directorios en el sistema.

**Información de estado:** Algunos programas obtienen información sobre la fecha, hora, memoria disponible, espacio en disco, número de usuarios y otros aspectos del sistema. Pueden presentar esta información en una ventana de interfaz gráfica o enviarla a dispositivos de salida.

**Modificación de archivos:** Se incluyen editores de texto que permiten crear y modificar el contenido de los archivos almacenados en la computadora. También puede haber comandos para buscar y reemplazar texto en los archivos.

**Soporte de lenguajes de programación:** Los sistemas operativos a menudo proporcionan compiladores, ensambladores, depuradores e intérpretes para varios lenguajes de programación populares.

**Carga y ejecución de programas:** Estos programas se utilizan para cargar programas en memoria y ejecutarlos. Pueden incluir cargadores absolutos, cargadores reubicables y herramientas de depuración.

**Comunicaciones:** Estos programas permiten la comunicación entre procesos, usuarios y computadoras. Incluyen herramientas para enviar mensajes, explorar la web, enviar correos electrónicos, iniciar sesiones remotas y transferir archivos.

Además de los programas del sistema, los sistemas operativos a menudo se suministran con programas de utilidad que resuelven problemas comunes o realizan tareas frecuentes, como exploradores web, procesadores de texto, hojas de cálculo, sistemas de bases de datos, paquetes gráficos, juegos y más. Estos programas se conocen como utilidades del sistema o programas de aplicación.

# Diseño e implementación del sistema operativo

### Objetivos del diseño

Es esencial definir claramente los objetivos y especificaciones del sistema. Estos objetivos pueden dividirse en dos grupos: objetivos del usuario y objetivos del sistema.

Los objetivos del usuario incluyen la comodidad de uso, facilidad de aprendizaje, fiabilidad, seguridad y velocidad. Estos objetivos se centran en la experiencia del usuario y en su capacidad para interactuar efectivamente con el sistema.

Los objetivos del sistema se refieren a la facilidad de diseño, implementación y mantenimiento del sistema, su flexibilidad, fiabilidad, ausencia de errores y eficiencia en su funcionamiento. Estos objetivos se centran en la construcción y operación efectiva del sistema.

No existe una solución única para definir los requisitos de un sistema operativo, ya que estos pueden variar según el entorno y el propósito del sistema. El diseño de un sistema operativo es una tarea creativa que se basa en principios generales de ingeniería de software.

En última instancia, el diseño de un sistema operativo debe equilibrar los objetivos del usuario y del sistema para crear un sistema que satisfaga las necesidades de los usuarios mientras se mantiene de manera eficiente y confiable.

### Mecanismos y políticas

un principio importante en el diseño de sistemas operativos es la separación de políticas y mecanismos. Los mecanismos se encargan de cómo se realiza una tarea, mientras que las políticas definen qué se debe hacer en una situación dada. Esta separación es fundamental para lograr flexibilidad en el diseño de sistemas operativos.

La ventaja de separar políticas y mecanismos radica en la capacidad de adaptar el sistema a diferentes situaciones o cambios en las políticas sin necesidad de modificar los mecanismos subyacentes. Por ejemplo, un mecanismo de asignación de prioridades puede utilizarse para implementar diferentes políticas de planificación de CPU, como dar prioridad a procesos intensivos en E/S sobre los procesos intensivos en CPU, o viceversa, sin cambiar el mecanismo en sí.

Los sistemas operativos basados en microkernel llevan esta separación al extremo, al implementar un conjunto básico de componentes primitivos que son independientes de políticas específicas. Los usuarios pueden agregar políticas y mecanismos avanzados a través de módulos del kernel o programas de usuario.

Por otro lado, sistemas como Windows o Mac OS X tienden a codificar tanto mecanismos como políticas en el sistema, lo que limita la flexibilidad y estandariza la experiencia del usuario en términos de interfaz y comportamiento de las aplicaciones.

### Implementación

la implementación de un sistema operativo generalmente se realiza en lenguajes de alto nivel, como C o C++, en lugar de lenguaje ensamblador. Esto proporciona varias ventajas, como un desarrollo más rápido, código más compacto, facilidad para entender y depurar, y la capacidad de portar el sistema operativo a diferentes arquitecturas de hardware de manera más sencilla.

Las posibles desventajas relacionadas con el rendimiento y el uso de espacio de almacenamiento se han vuelto menos significativas en los sistemas modernos, ya que los compiladores modernos pueden generar código eficiente y optimizado. La optimización del código en lenguaje ensamblador solo se considera en casos críticos de rendimiento, como las partes del sistema operativo que gestionan la memoria y la planificación de la CPU.

Para identificar cuellos de botella y mejorar el rendimiento, es esencial monitorear el comportamiento del sistema. Se agregan funciones de registro de eventos y rendimiento al sistema operativo para recopilar información detallada sobre su funcionamiento. Luego, se utilizan programas de análisis para procesar estos registros y detectar ineficiencias o áreas críticas que puedan requerir optimización. Además, las trazas también son útiles para verificar y validar mejoras propuestas antes de su implementación. También pueden ayudar a los desarrolladores a encontrar errores en el comportamiento del sistema operativo.

## Estructura del sistema operativo

### Estructura simple

algunos sistemas operativos comerciales no tienen una estructura bien definida desde el principio. A menudo, comienzan como sistemas pequeños y simples y luego crecen más allá de su diseño original. Un ejemplo de esto es MS-DOS, que fue desarrollado inicialmente por un grupo pequeño sin la previsión de su futura popularidad. Debido a su enfoque en proporcionar funcionalidad en un espacio mínimo, MS-DOS no se dividió en módulos cuidadosamente estructurados, lo que resultó en la falta de separación entre interfaces y niveles de funcionalidad. Esto hizo que MS-DOS fuera vulnerable a fallas de programas de usuario, lo que podría causar la caída del sistema completo.

Otro ejemplo es el sistema operativo UNIX original, que también se vio limitado por la funcionalidad del hardware en sus primeras etapas. UNIX consiste en dos partes separadas: el kernel y los programas del sistema. El kernel, a lo largo del tiempo, se dividió en una serie de interfaces y controladores de dispositivos. Aunque esta división en niveles es más estructurada que MS-DOS, todavía se considera una estructura monolítica debido a la cantidad significativa de funcionalidad que se encuentra en un solo nivel.

En ambos casos, estas estructuras limitadas dificultaron la implementación y el mantenimiento del sistema operativo a medida que crecía y evolucionaba.

### Estructura en niveles

el diseño modular de sistemas operativos es fundamental para su desarrollo y mantenimiento. Un enfoque eficaz es la estructuración del sistema en niveles, donde cada nivel representa una implementación de un objeto abstracto con datos y operaciones. Los niveles se organizan de manera jerárquica, con el hardware en el nivel más bajo y la interfaz de usuario en el nivel más alto.

Las ventajas del enfoque de niveles incluyen:

**Simplificación de la construcción y depuración:** Cada nivel puede depurarse de manera independiente, ya que solo utiliza las operaciones de los niveles inferiores, lo que facilita la identificación y corrección de errores.

**Ocultación de detalles:** Cada nivel oculta los detalles de implementación a los niveles superiores, lo que permite a los programadores enfocarse en la interfaz y las operaciones sin preocuparse por cómo se implementan.

Sin embargo, este enfoque también presenta desafíos, como la necesidad de una planificación cuidadosa para definir adecuadamente los diferentes niveles y evitar conflictos de dependencia. Además, la implementación basada en niveles tiende a ser menos eficiente en términos de rendimiento debido a la sobrecarga de llamadas a niveles en cascada.

En los diseños más recientes de sistemas operativos, se ha optado por utilizar menos niveles con mayor funcionalidad en cada uno, lo que combina las ventajas de la modularidad con una mejor eficiencia y una gestión más flexible de las operaciones.

### Microkernels

l concepto de microkernel surgió como una solución para modularizar sistemas operativos y mejorar su mantenimiento y extensibilidad. Un microkernel es un kernel mínimo que se encarga de proporcionar servicios básicos como gestión de memoria, procesos y comunicaciones, mientras que otras funcionalidades se implementan como programas de nivel de usuario. Esto tiene varias ventajas:

**Tamaño reducido del kernel:** El microkernel es más pequeño y contiene solo las funciones esenciales, lo que facilita su gestión y mantenimiento.

**Facilidad de extensión:** Agregar nuevos servicios al sistema operativo se vuelve más sencillo, ya que se implementan como programas de usuario sin modificar el kernel.

**Seguridad y fiabilidad:** Dado que la mayoría de los servicios se ejecutan como procesos de usuario en lugar de procesos del kernel, los fallos en un servicio no afectan al resto del sistema operativo, lo que mejora la seguridad y la estabilidad.

**Portabilidad:** El sistema operativo resultante es más fácil de portar a diferentes arquitecturas de hardware.

Sin embargo, los microkernels también pueden tener un rendimiento inferior debido a la sobrecarga de procesamiento generada por la comunicación entre servicios a través de mensajes. En algunos casos, como Windows NT, se han realizado cambios en la arquitectura del sistema operativo para abordar problemas de rendimiento, lo que ha llevado a una reevaluación de la estructura del microkernel.

En la práctica, sistemas operativos como Tru64 UNIX (Digital UNIX) y QNX han utilizado el enfoque de microkernel para proporcionar un entorno modular y seguro. A pesar de las preocupaciones de rendimiento, los microkernels siguen siendo una opción viable para ciertas aplicaciones y entornos donde la modularidad y la seguridad son prioritarias.

### Módulos

Una metodología actualmente eficaz para el diseño de sistemas operativos es la utilización de técnicas de programación orientada a objetos para crear un kernel modular. En este enfoque, el kernel consta de un conjunto de componentes fundamentales y enlaza dinámicamente servicios adicionales, ya sea durante el arranque del sistema o en tiempo de ejecución. Esta estrategia se utiliza en implementaciones modernas de sistemas operativos como Solaris, Linux y macOS.

La estructura del sistema operativo Solaris, por ejemplo, se organiza alrededor de un kernel central con varios tipos de módulos de kernel cargables, que incluyen:

- Clases de planificación.
- Sistemas de archivos.
- Llamadas al sistema cargables.
- Formatos ejecutables.
- Módulos STREAMS.
- Módulos misceláneos.
- Controladores de bus y dispositivos.

Este diseño permite al kernel proporcionar servicios básicos mientras permite la implementación dinámica de características adicionales. Por ejemplo, se pueden agregar controladores de hardware específicos al kernel y añadir soporte para sistemas de archivos mediante módulos cargables. El resultado es similar a un sistema de niveles en el sentido de que cada sección del kernel tiene interfaces bien definidas y protegidas, pero es más flexible, ya que cualquier módulo puede comunicarse con cualquier otro sin necesidad de un mecanismo de paso de mensajes. Además, es más eficiente que un microkernel porque los módulos pueden comunicarse de manera más directa.

Por otro lado, el sistema operativo macOS (también conocido como Darwin), utilizado en las computadoras Apple Macintosh, utiliza una estructura híbrida. Combina una técnica de niveles con el microkernel Mach. Los niveles superiores incluyen entornos de aplicación y servicios que ofrecen una interfaz gráfica a las aplicaciones. El entorno del kernel, por debajo de estos niveles, consta principalmente del microkernel Mach y el kernel BSD. Mach se encarga de la gestión de memoria, el soporte para llamadas a procedimientos remotos y facilidades de comunicación interprocesos, incluyendo un mecanismo de paso de mensajes. El kernel BSD proporciona una interfaz de línea de comandos BSD, soporte para red y sistemas de archivos, así como una implementación de las API de POSIX. El entorno del kernel también ofrece un kit de E/S para el desarrollo de controladores de dispositivo y módulos dinámicamente cargables. Las aplicaciones y servicios comunes pueden utilizar directamente las facilidades de Mach o BSD.

Este enfoque modular y orientado a objetos permite una mayor flexibilidad y extensibilidad en el diseño de sistemas operativos modernos, lo que facilita la incorporación de nuevas características y servicios sin la necesidad de reescribir todo el sistema desde cero.

# Maquinas virtuales

El concepto de máquina virtual se basa en la abstracción del hardware de una computadora, incluyendo la CPU, la memoria, las unidades de disco y más, para crear múltiples entornos de ejecución que dan la ilusión de que cada uno de ellos opera en su propia computadora privada. Esto se logra mediante mecanismos de planificación de la CPU y técnicas de memoria virtual que permiten que cada proceso tenga su propia copia virtual de los recursos de hardware subyacentes.

Una máquina virtual no proporciona las características adicionales como llamadas al sistema y sistemas de archivos, pero ofrece una interfaz que es idéntica al hardware básico subyacente. Cada proceso opera como si tuviera su propia computadora independiente.

Las ventajas de las máquinas virtuales incluyen la capacidad de compartir el mismo hardware entre múltiples entornos de ejecución diferentes, lo que permite la ejecución concurrente de diferentes sistemas operativos. Un ejemplo de sistema operativo que utiliza el concepto de máquina virtual es el sistema VM de IBM.

Una de las dificultades clave en la implementación de máquinas virtuales es la gestión de los sistemas de disco. Cuando la máquina física tiene un número limitado de unidades de disco y se ejecutan múltiples máquinas virtuales, se utilizan discos virtuales (minidiscos) que son idénticos en todo, excepto en tamaño. Cada minidisco se implementa asignando pistas de los discos físicos según sea necesario. La suma de los tamaños de todos los minidiscos debe ser menor que el espacio de disco físico disponible.

En sistemas VM de IBM, los usuarios ejecutan normalmente el sistema operativo CMS, que es interactivo y monousuario. El software de la máquina virtual se encarga de multiprogramar múltiples máquinas virtuales en una sola máquina física sin preocuparse por el software de soporte al usuario. Esta arquitectura divide eficazmente el problema de diseño de un sistema interactivo multivariado en dos partes más manejables.

### implementación

La implementación de una máquina virtual es una tarea compleja debido a la necesidad de replicar la funcionalidad de la máquina subyacente en un entorno virtual. La máquina subyacente tiene dos modos de operación: modo usuario y modo kernel, y el software de la máquina virtual debe ejecutarse en modo usuario. Por lo tanto, la máquina virtual debe tener sus propios modos de usuario virtual y kernel virtual, ambos ejecutándose en modo usuario físico.

La transición del modo usuario virtual al modo kernel virtual en una máquina virtual se logra de la siguiente manera: cuando un programa que se ejecuta en modo usuario virtual realiza una llamada al sistema o intenta ejecutar una instrucción privilegiada, se produce una transferencia al monitor de la máquina virtual en la máquina real. Una vez que el monitor de la máquina virtual obtiene el control, puede modificar los registros y el contador de programa para que la máquina virtual simule el efecto de la llamada al sistema y luego reinicie la máquina virtual en modo kernel virtual.

Es importante tener en cuenta que la ejecución en una máquina virtual puede ser más rápida o más lenta que en una máquina física, dependiendo de varios factores. La entrada/salida (E/S) virtual puede ser más rápida o más lenta que la E/S real, y la multiprogramación de la CPU entre varias máquinas virtuales puede afectar la velocidad de ejecución de las máquinas virtuales de manera impredecible.

En casos extremos, puede ser necesario simular todas las instrucciones para proporcionar una máquina virtual verdadera. Sin embargo, en sistemas como VM de IBM, las instrucciones normales de las máquinas virtuales pueden ejecutarse directamente por hardware. Solo las instrucciones privilegiadas, necesarias principalmente para operaciones de E/S, deben simularse y ejecutarse de manera más lenta.

La implementación de máquinas virtuales puede ser un desafío técnico significativo debido a la necesidad de replicar de manera efectiva el hardware subyacente y garantizar que las máquinas virtuales funcionen de manera adecuada y eficiente.

### Beneficios

El concepto de máquina virtual presenta una serie de beneficios:

**Protección completa de recursos:** En un entorno de máquina virtual, cada máquina virtual está completamente aislada de las demás, lo que garantiza una protección completa de los recursos del sistema. Esto significa que no hay problemas de protección entre máquinas virtuales, lo que aumenta la seguridad y la confiabilidad del sistema.

**Compartición de recursos:** Aunque las máquinas virtuales están aisladas, es posible compartir recursos mediante mecanismos implementados por software. Por ejemplo, se pueden compartir discos y archivos a través de discos virtuales compartidos. También es posible definir una red virtual que permita la comunicación entre las máquinas virtuales, lo que facilita la colaboración y la comunicación.

**Entorno de desarrollo seguro:** Las máquinas virtuales son ideales para la investigación y el desarrollo de sistemas operativos. Modificar un sistema operativo en una máquina física puede ser arriesgado y complicado, ya que los sistemas operativos son complejos y un error podría causar problemas graves. Con una máquina virtual, los programadores pueden realizar cambios y pruebas en un entorno aislado y seguro, sin interrumpir la operación normal del sistema. Esto reduce el tiempo de desarrollo del sistema y evita interrupciones en el servicio.

### VM ware

VMware es una aplicación comercial que proporciona virtualización de hardware en sistemas x86 de Intel. Funciona como una aplicación en un sistema operativo host, como Windows o Linux, y permite la ejecución concurrente de múltiples sistemas operativos invitados como máquinas virtuales independientes.

Este software es útil en situaciones donde un desarrollador necesita probar una aplicación en diferentes sistemas operativos, como Linux, FreeBSD, Windows NT y Windows XP. En lugar de requerir múltiples computadoras físicas o reinstalar sistemas operativos, VMware permite ejecutar estos sistemas simultáneamente como máquinas virtuales en una única computadora física.

VMware abstrae el hardware físico y crea máquinas virtuales aisladas, cada una con sus recursos virtuales, como CPU, memoria, unidades de disco y interfaces de red. Esto proporciona un entorno separado y seguro para ejecutar sistemas operativos invitados.

### JVM Java Virtual Machine

La JVM es una especificación de una computadora abstracta que consta de un cargador de clases y un intérprete de Java que ejecuta código intermedio Java, conocido como bytecode. La JVM es neutral en cuanto a la arquitectura y puede ejecutar programas Java en diferentes sistemas operativos.

La JVM se puede implementar por software en sistemas operativos host, como Windows, Linux o Mac OS X, o incluso como parte de un navegador web. También es posible implementarla por hardware en chips específicamente diseñados para ejecutar programas Java de manera eficiente.

Para acelerar la ejecución de programas Java, se utilizan técnicas como la compilación "just-in-time" (JIT), donde el código intermedio se convierte en código máquina nativo la primera vez que se invoca un método y se almacena en caché para futuras invocaciones. Otra técnica es la ejecución de la JVM por hardware, que utiliza un chip Java especializado para ejecutar operaciones en código intermedio Java como código nativo, eliminando la necesidad de un intérprete o compilador JIT.

En resumen, VMware proporciona virtualización de hardware para ejecutar múltiples sistemas operativos en una única computadora física, mientras que la JVM es una máquina virtual que permite ejecutar programas Java en diferentes sistemas operativos de manera eficiente. Ambas tecnologías son útiles para simplificar el desarrollo y la ejecución de aplicaciones en entornos heterogéneos.

## Generación de sistemas operativos

La generación de sistemas operativos es un proceso mediante el cual se adapta o configura un sistema operativo para funcionar en una máquina de hardware específica o en una instalación particular. En lugar de diseñar y desarrollar un sistema operativo desde cero para cada configuración, se utiliza un programa especial llamado "SYSGEN" o "system generation" para personalizar el sistema operativo de acuerdo con las características del hardware y las preferencias del usuario.

El proceso de generación de un sistema operativo generalmente implica la obtención de información específica sobre la configuración del hardware y las preferencias del sistema, que puede incluir:

- Información sobre la CPU, como el tipo de CPU, las extensiones de instrucciones disponibles y otras características relacionadas con el procesador.

- La cantidad de memoria disponible en la máquina.

- La lista de dispositivos instalados, incluyendo su número de dispositivo, número de interrupción, tipo y modelo, y cualquier otra característica relevante.

- Opciones de configuración del sistema operativo, como el número de búferes a utilizar, el algoritmo de planificación de la CPU, el número máximo de procesos a soportar, entre otros.

Una vez recopilada esta información, se puede utilizar de varias maneras para generar el sistema operativo personalizado:

- Personalización del código fuente: Un administrador de sistemas puede modificar el código fuente del sistema operativo para adaptarlo a la configuración específica. Esto implica cambios en las declaraciones de datos, valores de inicialización y constantes, así como la compilación del sistema operativo completo.

- Montaje de módulos precompilados: En un enfoque menos personalizado, se pueden seleccionar módulos de una biblioteca precompilada y montarlos para construir el sistema operativo final. Esto permite una generación más rápida del sistema, pero puede resultar en un sistema más genérico.

- Control basado en tablas: Se puede construir un sistema operativo que se controla completamente mediante tablas. Todo el código forma parte del sistema y la selección de componentes se realiza en tiempo de ejecución en lugar de en tiempo de compilación o montaje. La generación del sistema implica la creación de tablas que describen el sistema.

Las diferencias clave entre estos métodos incluyen el tamaño y la generalidad del sistema resultante, así como la facilidad para realizar modificaciones cuando cambia la configuración del hardware. La elección del método depende de las necesidades específicas y la frecuencia de los cambios en la configuración del sistema. En resumen, la generación de sistemas operativos permite adaptar un sistema operativo a una configuración de hardware específica o preferencias del usuario de manera eficiente.

## Arranque del sistema

El proceso de inicio de una computadora, conocido como "arranque del sistema", implica la inicialización y carga del kernel del sistema operativo en la memoria principal para su ejecución. En la mayoría de los sistemas informáticos, este proceso se realiza a través de un programa de inicio o cargador de inicio, que se encuentra en una memoria de solo lectura (ROM) y es responsable de ubicar y cargar el kernel en la memoria. En algunos sistemas, como los teléfonos móviles y consolas de juegos, todo el sistema operativo se almacena en ROM debido a su simplicidad y entorno de operación específico.

El programa de inicio puede realizar varias tareas, incluyendo diagnósticos para verificar el estado de la máquina y la inicialización de diversos componentes del sistema, como registros de la CPU y controladores de dispositivos. Después de completar estas tareas, el programa de inicio inicia la ejecución del sistema operativo.

Existen diferentes enfoques para el almacenamiento del sistema operativo y el proceso de arranque:

**Almacenamiento en ROM:** Algunos sistemas almacenan todo el sistema operativo en ROM, lo que es adecuado para sistemas pequeños y dispositivos con hardware simple. Cambiar el código de inicio en este caso requiere la modificación de chips ROM.

**EPROM (memoria de solo lectura programable y borrable):** Algunos sistemas utilizan EPROM, que permite escribir y modificar el contenido de ROM mediante comandos específicos. Esto ofrece flexibilidad para cambiar el código de inicio.

**Carga desde disco:** En sistemas más grandes o que cambian con frecuencia, el programa de inicio se almacena en ROM y el sistema operativo en disco. El programa de inicio realiza diagnósticos y luego lee un bloque fijo del disco (generalmente el bloque cero) que contiene información sobre cómo cargar el sistema operativo en memoria y ejecutarlo.

Una vez que el programa de inicio ha cargado el sistema operativo en memoria, este último puede explorar el sistema de archivos para ubicar el kernel del sistema operativo, cargarlo en memoria principal y comenzar su ejecución. Solo en este punto se considera que el sistema está en funcionamiento.

En resumen, el proceso de arranque del sistema implica la carga del kernel del sistema operativo en memoria y su ejecución, lo que se logra a través de un programa de inicio que puede almacenarse en ROM o cargarse desde un disco.


# Resumen

- Los sistemas operativos ofrecen una variedad de servicios a los usuarios y programas que se ejecutan en una computadora. Estos servicios se dividen en diferentes niveles. En el nivel más bajo, las llamadas al sistema permiten que los programas soliciten servicios directamente al sistema operativo. En niveles superiores, el intérprete de comandos o shell proporciona una interfaz para que los usuarios ejecuten solicitudes sin necesidad de programar. Estas solicitudes pueden provenir de archivos de procesamiento por lotes o directamente de un terminal en modo interactivo o de tiempo compartido.

- Los servicios proporcionados por un sistema operativo se pueden clasificar en varias categorías, que incluyen el control de programas, solicitudes de estado y solicitudes de entrada/salida (E/S). Además, los errores de los programas pueden considerarse como solicitudes implícitas de servicio.

- El diseño de un nuevo sistema operativo es una tarea compleja que requiere una planificación cuidadosa. Es esencial definir claramente los objetivos del sistema antes de comenzar el diseño, ya que estos objetivos dictarán las decisiones sobre algoritmos y estrategias a utilizar. La modularidad es un principio clave en el diseño de sistemas operativos, y se pueden utilizar enfoques como la estructura en niveles o un microkernel para lograrlo. El concepto de máquina virtual se basa en una arquitectura en niveles y permite cargar otros sistemas operativos sobre esta máquina virtual.

- A lo largo del ciclo de diseño del sistema operativo, es importante separar las decisiones de política de los detalles de implementación (mecanismos) para garantizar la flexibilidad futura si es necesario realizar cambios en la política. Los sistemas operativos suelen escribirse en lenguajes de implementación de sistemas o lenguajes de alto nivel para facilitar la implementación, el mantenimiento y la portabilidad.

- Una vez que se ha diseñado el sistema operativo, se debe llevar a cabo la generación del sistema para que esté listo para su uso. Esto implica la inicialización de la CPU y la ejecución de un programa de arranque almacenado en firmware. Este programa de arranque puede cargar el sistema operativo en memoria desde el firmware o desde el disco, permitiendo que el sistema informático comience a funcionar.