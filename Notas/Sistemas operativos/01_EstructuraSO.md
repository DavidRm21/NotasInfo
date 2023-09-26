
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

