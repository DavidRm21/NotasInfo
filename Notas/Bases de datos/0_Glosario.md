# Glosario de palabras RDBMS

## Contenido

[1. Instancias / Instance](#instance)

[2. Esquema / Schema](#schema)

[3. Tabla / Table](#table)

[4. Columna / Column](#column)

[5. Fila / Row](#row)

[6. Llave primaria / Primary key](#primary-key)

[7. Llave foránea / Foreign key](#foreign-key)

[8. Índice / Index](#index)

[9. Consulta / Query](#query)

[10. SQL](#sql-lenguaje-de-consulta-estructurado)

[11. SELECT](#sentencia-select)

[12. WHERE](#cláusula-where)

[13. JOIN](#join)

[14.  Normalization / Normalización](#normalización)

[15.  Denormalization / Desnormalización](#desnormalización)

[16. Propiedades ACID / ACID properties](#acid-properties)

[17. Vistas / View](#view)

[18. Procedimiento almacenado / Stored Procedure](#stored-procedure)

[19. Disparador / Trigger](#trigger)

[20. Copia de seguridad / Backup](#backup)

[21. Recuperación / Recovery](#recovery)

[22. Registro de rehacer / Redo Log](#redo-log)

[23. Archivado / Archiving](#archiving)

[24. Diccionario de datos / Data dictionary](#data-dictionary)

[25. Privilegios / Privileges](#privileges)

[26. Rol / Role](#role)

[27. Instance Crash](#instance-crash)

[28. PL/SQL](#plsql)

[29. LOB](#lob)

[30. OLTP](#oltp)

[31. OLAP](#olap)

[32. Requerimientos funcionales y no funcionales](#requerimientos-funcionales-y-no-funcionales)

[33. Modelo Entidad / Relación vs modelo relacional]()

#### **Instance**: 
Un entorno de base de datos Oracle en ejecución asociado a estructuras de memoria y procesos en segundo plano.

![Entorno SQL](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi.stack.imgur.com%2FEbB8v.png&f=1&nofb=1&ipt=43c243030719d53f25f17c9a8649d83f36470e08a6177864929f69d1f37ce1dd&ipo=images)

#### **Schema**: 
Un contenedor lógico para objetos de base de datos como tablas, vistas e índices, propiedad de un usuario.

![Esquema sql](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fi.ytimg.com%2Fvi%2FKECvDwc9E3A%2Fmaxresdefault.jpg&f=1&nofb=1&ipt=a64acf2a0d4cf34dfe0ad2b8a48a8d7aed0838d3cb276ea5becba83d1bd15033&ipo=images)

#### **Table**: 
Se utiliza para organizar y almacenar datos en forma de filas y columnas. Cada fila representa un registro o una entrada en la tabla, mientras que cada columna representa un atributo o campo específico de esos registros.

![Tabla oracle](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi.stack.imgur.com%2F8dQ3C.jpg&f=1&nofb=1&ipt=ce96266bd9ee94138b8d11f1280f4702a8cc566510c126d71182b1dfba779be0&ipo=images)

#### **Column**: 
Elemento de datos vertical de una tabla que contiene tipos específicos de datos.

#### **Row**: 
Elemento de datos horizontal de una tabla que representa un único registro de datos.

#### **Primary key**: 
Identificador único de una fila de una tabla, que garantiza la integridad de los datos y permite realizar búsquedas eficaces.

#### **Foreign Key**: 
Campo que establece un vínculo entre dos tablas, garantizando la integridad referencial.

![Primary / Foreign Key](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Flh5.googleusercontent.com%2Fproxy%2FZPmie_elJ9TZrL4aia_ZBQpqqhn7UuKr78kX__8AikKPm2wyajQyfAA8zcpyssacUzsf91lhsgwLSX3yEfA83SzPeFfdamTKUwjrEIE3QK2giHO7cUekUvs%3Dw1200-h630-p-k-no-nu&f=1&nofb=1&ipt=2f9aae8c55e3686a7554ab06656b096a30dc9dcc710303cc7c08cdb97f050b26&ipo=images)

#### **Index**: 
Estructura de datos que mejora la velocidad de recuperación de datos al proporcionar una forma rápida de localizar filas en una tabla.

![indice](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftechgoeasy.com%2Fwp-content%2Fuploads%2F2016%2F03%2Fb-tree_index.png&f=1&nofb=1&ipt=6aedd071f8cce73d5a564e6dd1eed4844cc1e8944db084d61f8b7cc3cc4ae390&ipo=images)

#### **Query**: 
Solicitud de información a la base de datos mediante SQL.

#### **SQL (Lenguaje de consulta estructurado)**: 
Lenguaje utilizado para comunicarse con bases de datos relacionales y gestionarlas.

#### **Sentencia SELECT**: 
Una sentencia SQL utilizada para recuperar datos de una o más tablas.

#### **Cláusula WHERE**: 
Cláusula utilizada en SQL para filtrar filas en función de una condición especificada.

#### **JOIN**: 
Combinación de datos de varias tablas basada en columnas relacionadas.

![querys](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fus.v-cdn.net%2F6032257%2Fuploads%2F0XCVSN49IVDP%2Fimage.png&f=1&nofb=1&ipt=678a617df81627d68539711734952d1de7540fa608eff4ee0e31bc2a55e0aace&ipo=images)

#### **Normalización**: 
Proceso de diseño de un esquema de base de datos para minimizar la redundancia de datos y garantizar su integridad.

#### **Desnormalización**: 
Introducción intencionada de redundancia para mejorar el rendimiento de la consulta.

#### **Transaction**: 
Una única unidad de trabajo o una serie de acciones que deben tratarse como un todo.

#### **ACID Properties**: 
Conjunto de propiedades (*Atomicidad, Consistencia, Aislamiento, Durabilidad*) que garantizan un procesamiento fiable de las transacciones de una base de datos.

![Acid](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fblog.sqlauthority.com%2Fwp-content%2Fuploads%2F2016%2F04%2Facid.png&f=1&nofb=1&ipt=b81ffad63ef24500dcd07a4fb53d1bcfea510253ae34df7ae68968d99f7a99cb&ipo=images)

#### **View**: 
Tabla virtual derivada de una o más tablas o vistas, que presenta los datos de una forma específica.

#### **Stored procedure**: 
Una colección precompilada de una o más sentencias SQL que pueden ejecutarse como una sola unidad.

![Stored procedure](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi.ytimg.com%2Fvi%2FW6OpuZCA4LM%2Fmaxresdefault.jpg&f=1&nofb=1&ipt=5fcc7ab1b59efd8c6f163fe58a0ba2b53b43b201db98d1599285eb4ab2bb5e19&ipo=images)

#### **Trigger**: 
Objeto de base de datos que se ejecuta automáticamente en respuesta a eventos especificados.

![Trigger example](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi.ytimg.com%2Fvi%2FgA79wEpFFGM%2Fmaxresdefault.jpg&f=1&nofb=1&ipt=5623edca12a4a1445687188430929b9dc50fbcaa68a57bf62eac41ec39a8a72a&ipo=images)

#### **Backup**: 
Copia de datos utilizada para restaurar la base de datos en caso de pérdida o corrupción de datos.

#### **Recovery**: 
El proceso de restaurar la base de datos a un estado consistente después de un fallo.

#### **Redo Log**: 
Conjunto de archivos que registran los cambios realizados en la base de datos, esencial para la recuperación.

#### **Archiving**: 
Traslado de los archivos de redo log llenos a una ubicación diferente para su almacenamiento a largo plazo.

#### **Data Dictionary**: 
Una colección de metadatos sobre la estructura y los objetos de la base de datos.

![Dictionaries](Oracle+Data+Dictionary+Views-2698940867.jpg)

#### **Privileges**: 
Permisos que controlan el acceso de un usuario a objetos específicos de la base de datos.

![Privilegios](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fimage1.slideserve.com%2F1868670%2Fprivileges-in-oracle-l.jpg&f=1&nofb=1&ipt=c82a6d75d2d1d7ce264b88ff443dfb9983969d9b5dee36cad4f5dbf6c8dd6792&ipo=images)

#### **Role**: 
Un grupo nombrado de privilegios que se pueden conceder a los usuarios.

#### **Instance Crash**: 
Cuando la instancia de Oracle termina anormalmente debido a un error o fallo de hardware.

***

### PL/SQL 
Permite realizar tareas más avanzadas dentro de la base de datos de Oracle, como automatizar procesos, realizar cálculos complejos y mantener la integridad de los datos mediante la definición de reglas y restricciones personalizadas.

| SQL | PL/SQL |
|-----|--------|
| Es el lenguaje utilizado para realizar consultas y operaciones en las bases de datos. Se utiliza para recuperar, insertar, actualizar y eliminar datos en las tablas.    |  Es un lenguaje que extiende las capacidades de SQL al permitirte escribir programas o bloques de código que se ejecutan directamente en la base de datos. Esto significa que puedes crear procedimientos, funciones, desencadenadores y otros elementos de lógica de programación en la base de datos.      |

### LOB: 
Tipo de datos para almacenar datos grandes como imágenes, archivos de sonido y documentos.

![LOB](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fwww.oracle.com%2Ftechnetwork%2Fes%2Fimages%2Foracle-large-objects-16-1936996.gif&f=1&nofb=1&ipt=a1ef254a8cd32ac09eab018e2338dd669da4514df0ea788cdfa31c6974c9ad0a&ipo=images)

### OLTP: 
Sistema de procesamiento de transacciones en tiempo real para operaciones individuales.

![OLTP](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcf2.ppt-online.org%2Ffiles2%2Fslide%2F9%2F9LvRKgrijNpd85nSGcZmDwf62UH3alzXoqOY7eBkI%2Fslide-9.jpg&f=1&nofb=1&ipt=3454effc8e09806957c62aa0ddd639bc51b5e9cd48166c8cd0372ca4a00497f6&ipo=images)

### OLAP: 
Sistema de procesamiento analítico para consultas complejas en datos históricos o multidimensionales.

![OLAP](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse1.mm.bing.net%2Fth%3Fid%3DOIP._w5diJh9xwfH2ZGSXeSPAwHaE8%26pid%3DApi&f=1&ipt=cd81f6daaba6d979a4eb54c39c4434c1a7c56e9b1d0c27bed336c37711f1370c&ipo=images)

## Requerimientos funcionales y no funcionales

| R. funcional | R. no funcional |
|-----|--------|
|  Lo que el sistema debe hacer. Son las tareas y capacidades concretas que el sistema debe cumplir.  | Cómo debe hacerlo. Son las condiciones y características que determinan cómo el sistema debe comportarse, incluso si no se trata de funciones específicas.       |

***Ejemplo R. Funcional:***

- "El sistema debe permitir a los usuarios iniciar sesión con nombre de usuario y contraseña."
- "Los usuarios deben poder agregar nuevos registros a la base de datos."
- "Se debe poder ejecutar consultas SQL para recuperar información de la base de datos."

***Ejemplo R. no funcional:***

- "El sistema debe responder a las consultas en menos de 2 segundos."
- "Debe ser capaz de manejar simultáneamente al menos 1000 usuarios."
- "La base de datos debe ser segura y solo accesible por usuarios autorizados."

### Modelo Entidad/Relación vs Modelo relacional

Son dos enfoques diferentes para diseñar y representar bases de datos.

| E/R | Relacional |
|-----|--------|
|   Utiliza símbolos como círculos (entidades) y líneas (relaciones) para mostrar cómo las cosas están conectadas.    |    Las entidades se convierten en tablas, y las relaciones se convierten en cómo las tablas se relacionan entre sí. Utiliza filas y columnas para almacenar los datos de manera organizada.    |
|  El Modelo Entidad/Relación te ayuda a planificar cómo se verá tu base de datos   |    El Modelo Relacional es la forma real de organizar los datos en tablas y relaciones.     |

![modelo e/r y modelo relacional](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fjorgesanchez.net%2Fmanuales%2Fgbd%2Fdiseno-logico-relacional-web-resources%2Fimage%2F6.png&f=1&nofb=1&ipt=d785bcb3345fa594af49112acac441e257400f96931c720c5d7516b763db355a&ipo=images)
