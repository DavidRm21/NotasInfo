# Bases de datos relacionales

## Historia

Las bases de datos surgieron como respuesta a la necesidad de ***conservar información*** más allá de la memoria RAM. Inicialmente, se utilizaron bases de datos basadas en archivos de texto plano, que eran sencillas de almacenar pero complicadas de consultar de manera eficiente. **Edgar Codd**, el creador de las bases de datos relacionales, estableció reglas para garantizar que los principios fundamentales de las bases de datos se mantuvieran intactos y para estandarizar el proceso. Esto llevó al desarrollo de las bases de datos relacionales, que revolucionaron la manera en que se *almacena, organiza y accede a la información*, ofreciendo una estructura más coherente y potente para gestionar datos de manera efectiva.

## Las 12 reglas de CODD

[Recurso](https://www.w3resource.com/sql/sql-basic/codd-12-rule-relation.php)

***Regla de fundación / Regla 0:***

Todo sistema que se defina como sistema de gestión de base de datos relacional debe cumplir con 3 calificaciones:

- **Ser relacional:** El sistema debe ser capaz de manejar datos de manera relacionada, lo que significa que debe seguir las reglas y principios de las bases de datos relacionales.
- **Ser una base de datos:** El sistema debe ser capaz de almacenar y organizar datos de manera estructurada y eficiente.
- **Ser un sistema de gestión:**  El sistema debe ser capaz de administrar, controlar y permitir el acceso a la base de datos.

No deberá depender de caracteristicas externas para gestionar los datos.

1. ***Regla de la información / Regla 1:***

    La información debe guardarse en tablas con filas y columnas, de manera organizada y fácil de entender.

    ![Tabla con filas y columnas](https://jevq.files.wordpress.com/2013/03/tabla.png)

2. ***Regla del acceso garantizado / Regla 2:***

    Cada dato (valor atómico) debe ser accesible de manera lógica a traves de una combinación de nombre de tabla, valor de clave primaria y nombre de la columna, sin generar ambigüedad.

    ![Tabla PhpMyAdmin relacionada](https://parzibyte.me/blog/wp-content/uploads/2020/09/Tablas-relacionadas-en-MySQL.png)

3. ***Regla del tratamiento sistemático de valores nulos. / Regla 3:***

    Las bases de datos deben permitir valores "nulos" para representar información desconocida, de manera ordena y consistente.

    ![Tabla con valores nulos](https://guru99.es/wp-content/uploads/2018/04/a17_2.png)

4. ***Catálogo dinámico en línea basado en el modelo relacional / Regla 4:***

    La descripción de la base de datos, incluida su estructura y metadatos, debe ser accesible a través de un catálogo en línea utilizando el mismo lenguaje relacional, para que los usuarios puedan entenderla y consultarla. 

    ![Mapa de un modelo relacional](https://cmapspublic2.ihmc.us/rid=1P149L74D-PY71D1-4Q9K/Modelo%20relacional.png)

5. ***Regla del sublenguaje de datos completo / Regla 5:***

    Establece que debe existir al menos un lenguaje completo que sea capaz de abarcar todas las operaciones necesarias en una base de datos relacional. Este lenguaje debe ser capaz de definir datos, manipularlos, definir vistas, aplicar restricciones de integridad y gestionar la seguridad y las transacciones.

    ![Gestores de Bases de datos](https://i1.wp.com/www.diarlu.com/wp-content/uploads/2019/02/gestores_bases-datos.jpg?fit=1000%2C600&ssl=1)

6. ***Regla de actualización de vistas / Regla 6:***

    Establece que todas las vistas que puedan ser teóricamente actualizables deben ser actualizables por el sistema mismo.

    Esto garantiza que las vistas puedan ser utilizadas de manera efectiva y actualizadas sin problemas.

    ![Reglas de actualización](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fimages2018.cnblogs.com%2Fblog%2F1337265%2F201804%2F1337265-20180424144207849-1670791543.png&f=1&nofb=1&ipt=644f7f11e12d8b33711036ca720304f3179467437d530267fb1b6e0d7b6efa28&ipo=images)

7. ***Inserción, actualización y borrado de alto nivel / Regla 7:***

    Establece que un sistema de bases de datos debe ser capaz de manejar tanto la recuperación de datos (consultas) como las operaciones de inserción, actualización y borrado de manera integral para relaciones base o derivadas.

    Las cláusulas SELECT, UPDATE, DELETE e INSERT deben estar disponibles y funcionales para operar con registros, independientemente de las relaciones y restricciones que existan entre las tablas.

    ![Operaciones SQL](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fitmanabi.com%2Fwp-content%2Fuploads%2F2020%2F01%2FSQL-4-major.png&f=1&nofb=1&ipt=cd37348e04149f4736ed0c3144809344818271a081ee19ac514880539851ad4f&ipo=images)

8. ***Independencia física de los datos / Regla 8:***

    Establece que los cambios realizados en el nivel físico (cómo se almacenan los datos, ya sea en arreglos o listas enlazadas, entre otros) no deben requerir cambios en una aplicación basada en la estructura de los datos.

    Garantizar que los cambios en la forma en que se almacenan los datos no tengan un impacto negativo en las aplicaciones que acceden a esos datos.


9. ***Independencia lógica de los datos / Regla 9:***

    Establece que los cambios realizados en el nivel lógico de la base de datos (como las tablas, columnas, filas, etc.) no deben requerir modificaciones en las aplicaciones que se basan en la estructura de esos datos. La independencia lógica de los datos es más difícil de lograr que la independencia física de los datos.

    Requiere un diseño cuidadoso de la base de datos y de las interfaces de las aplicaciones para asegurarse de que los cambios en la estructura lógica no rompan la funcionalidad de las aplicaciones. 

    ![Independencia lógica](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2F3.bp.blogspot.com%2F-v025Qqd0NGE%2FV3-xCqlKyjI%2FAAAAAAAAAIE%2FYDkB4XPFVzAbbNiO5ymrbMRispDXhh2BACLcB%2Fs1600%2Fbase-de-datos-3-728.jpg&f=1&nofb=1&ipt=d8238b2835a555d90347fe08458807f5b56aa1d4b3dcd1263ac14a71c701ee4b&ipo=images)

10. ***Independencia de la integridad / Regla 10:***

    Las reglas que garantizan la integridad de los datos, como asegurarse de que los datos cumplan ciertos criterios (por ejemplo, no permitir valores nulos en una columna específica), deben ser definidas por separado de los programas que utilizan los datos. Estas restricciones deben almacenarse en el catálogo de la base de datos en lugar de estar incrustadas directamente en las aplicaciones.

    Esta regla contribuye a la flexibilidad y mantenibilidad de la base de datos y las aplicaciones, permitiendo que los cambios en las restricciones de integridad se realicen de manera más eficiente y controlada.

11. ***Independencia de la distribución / Regla 11:***

    Busca garantizar que los usuarios puedan continuar utilizando sus aplicaciones sin problemas, independientemente de los cambios en la distribución física de los datos. Esto es especialmente importante en entornos donde los datos se almacenan en múltiples ubicaciones para mejorar el rendimiento o la disponibilidad, ya que los usuarios no deben preocuparse por dónde se encuentran los datos ni cómo están distribuidos.

    *No debemos notar si la información está almacenada en diferentes lugares.*

12. ***La regla de la no subversión / Regla 12:***

    Evitar que los usuarios puedan utilizar interfaces de bajo nivel para realizar operaciones que no serían posibles o permitidas utilizando el enfoque relacional de alto nivel. Garantiza la coherencia y seguridad del sistema al evitar que las restricciones y políticas establecidas sean eludidas a través de métodos de acceso más directos y menos controlados.

    *Las formas avanzadas de acceder a la información no deben poder romper las reglas o evitar los controles que se han establecido.*


## ¿Qué son las entidades?

En el contexto de las bases de datos, una entidad es una representación de algo con existencia y significado en el mundo real o abstracto. Se asemeja a un objeto en la programación orientada a objetos y está destinada a ser almacenada y gestionada en la base de datos. Una entidad tiene atributos que describen sus características, propiedades o información relevante. Por convención, los nombres de las entidades se escriben en plural para indicar que se refieren a conjuntos de instancias.

## ¿Qué son los atributos?

Es una propiedad o característica que describe una entidad. Estos atributos proporcionan información específica sobre la entidad y ayudan a definir sus cualidades o propiedades distintivas.

- **Atributos:** Son las características o propiedades que se utilizan para describir una entidad. En un diagrama de entidad-relación, los atributos se representan generalmente dentro de óvalos y se conectan a la entidad correspondiente.

- **Atributos Compuestos:** Son atributos que están compuestos por sub-atributos. Es decir, un atributo compuesto en sí mismo tiene atributos que lo componen. Por ejemplo, una dirección podría ser un atributo compuesto con sub-atributos como calle, ciudad, estado, etc.

- **Atributos Clave:** Son atributos que identifican de manera única a una entidad dentro de una tabla o relación en la base de datos. Estos atributos no pueden repetirse y son utilizados para garantizar la unicidad en la identificación de las entidades.

- **Atributos Clave Naturales:** Son atributos clave que son inherentes al objeto o entidad. Por ejemplo, el número de serie de un producto.

- **Atributos Clave Artificiales:** Son atributos clave que son asignados de manera arbitraria para identificar una entidad. Por ejemplo, un ID generado automáticamente por el sistema

![Diagrama de chenn](https://static.platzi.com/media/user_upload/img-2e2fc1ba-ad77-4045-b7a5-f74a65e3f55e.jpg)

![Ejemplo diagrama de chenn](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.espai.es%2Fblog%2Fwp-content%2Fuploads%2F2015%2F05%2Fespai-introduccion-sql-e.jpg&f=1&nofb=1&ipt=3074861147e4d3e25e8159645e630d61d9b83edcd623b368288b8d547c3a6e55&ipo=images)

## Relaciones

Las relaciones son conexiones que permiten vincular o unir diferentes entidades en una base de datos. Se representan gráficamente con rombos en un diagrama entidad-relación y se definen mediante verbos que describen la naturaleza de la asociación entre las entidades.

## Cardinalidad

La cardinalidad en las relaciones se refiere a la cantidad de instancias de una entidad que pueden estar asociadas con el número correspondiente de instancias en la entidad relacionada. Se expresan en términos de números:

- **Cardinalidad 1 a 1:** Indica que una entidad en un lado de la relación está relacionada con exactamente una entidad en el otro lado, y viceversa.

- **Cardinalidad 0 a 1:** Indica que una entidad en un lado de la relación está relacionada con ninguna o una entidad en el otro lado, y viceversa.

- **Cardinalidad 1 a N:** Indica que una entidad en un lado de la relación está relacionada con al menos una entidad en el otro lado, pero puede estar relacionada con varias, y viceversa.

- **Cardinalidad 0 a N:** Indica que una entidad en un lado de la relación puede no estar relacionada o estar relacionada con varias entidades en el otro lado, y viceversa.

- **Cardinalidad N a N:** Esto significa que varias instancias de una entidad pueden estar relacionadas con varias instancias de la otra entidad, y viceversa. (*Entidad débil*)

![ejemplo cardinalidad](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Falvherre.cl%2Fpgsql%2FmodBasico%2Fent-rel-card.png&f=1&nofb=1&ipt=47e591f4c03c14ac6d981ac62b2b92e0011b18b8d8013a6b717df513322b0cc1&ipo=images)

## Diagrama ER

Es una herramienta visual utilizada para representar la estructura lógica y las relaciones entre las entidades en una base de datos. Es una forma gráfica de modelar la información y las interacciones en un sistema de bases de datos. Los Diagramas ER son ampliamente utilizados en el diseño y planificación de bases de datos.

![Ejemplo diagrama ER|Paltzi](https://static.platzi.com/media/user_upload/MDU-722a5797-ae44-4338-a501-5fb51196ceb3.jpg)

En un Diagrama ER:

- **Entidades:** Son representadas mediante rectángulos y representan objetos o conceptos en el mundo real que se almacenan en la base de datos.

- **Atributos:** Son características o propiedades de las entidades y se representan en óvalos conectados a las entidades.

- **Relaciones:** Son conexiones entre entidades que describen cómo interactúan o se asocian. Se representan mediante rombos y se definen mediante verbos.

- **Cardinalidad:** Se indica con números en los extremos de las líneas de relación y describe cuántas instancias de una entidad están conectadas a cuántas instancias de la otra entidad.

## Tipos de datos y constraints

![tipo de datos sql](https://static.platzi.com/media/user_upload/tiposDatos-0c0fdb12-4968-418a-8f7d-3b592c00da51.jpg)

![constraints sql](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.educba.com%2Facademy%2Fwp-content%2Fuploads%2F2019%2F10%2FSQL-Constraints.png&f=1&nofb=1&ipt=a6418f147e758e6e61b35e9b1336a18136d9f41a695e9e51cce9a4785c03d3d8&ipo=images)

- **NOT NULL:** No puede contener valores nulos

- **UNIQUE:** Asegura que cada valor en la columna sea único en toda la tabla, evitando duplicados.

- **PRIMARY KEY:** Es una combinación de las restricciones NOT NULL y UNIQUE. Define una columna o un conjunto de columnas como la clave principal de una tabla, lo que asegura la unicidad y la no nulidad.

- **FOREIGN KEY:** Identifica de manera única una fila en otra tabla. Establece una relación entre dos tablas, donde la columna que tiene la restricción FOREIGN KEY en una tabla referencia la clave principal en otra tabla.

- **CHECK:** Asegura que el valor en una columna cumpla una condición específica. 

- **DEFAULT:** Establece un valor por defecto para una columna cuando no se proporciona un valor explícito durante la inserción.

- **INDEX:** Crea una estructura de datos especial para permitir búsquedas más rápidas en la columna indexada. Mejora el rendimiento de consultas al acelerar la recuperación de datos.

# **Normalización**

La normalización es un proceso en el diseño de bases de datos que tiene como objetivo organizar y estructurar la información de manera eficiente y sin redundancias. 

![Sin normalizar](https://static.platzi.com/media/user_upload/sin-3a79e206-4b60-48ce-84d5-3645cce539d9.jpg)

La normalización se logra a través de varias formas normales, que son etapas de refinamiento que ayudan a eliminar la redundancia y aseguran la integridad de los datos.

- **Primera Forma Normal (1FN):** Requiere que los atributos de una tabla sean atómicos, es decir, no pueden contener campos repetidos ni valores compuestos. Cada celda debe contener un solo valor.

![Primera Forma](https://static.platzi.com/media/user_upload/Captura%20de%20Pantalla%202019-04-30%20a%20la%28s%29%2017.30.27-e38ed9bb-5d10-4f2b-acdc-fa2fa45433d3.jpg)

- **Segunda Forma Normal (2FN):** Además de cumplir con la 1FN, esta forma normal establece que cada campo de la tabla debe depender de la clave única completa (clave primaria).

![Segunda forma](https://static.platzi.com/media/user_upload/Captura%20de%20Pantalla%202019-04-30%20a%20la%28s%29%2017.26.28-2a12f9b9-2f11-4a1d-9cb0-23c2595cc260.jpg)

- **Tercera Forma Normal (3FN):** Cumple con la 1FN y 2FN, y agrega que los campos que no son parte de la clave primaria no deben tener dependencias funcionales transitivas, es decir, no deben depender de otros campos que no sean la clave primaria.

![Tercer forma](https://static.platzi.com/media/user_upload/3-89854a44-a4b2-4994-9975-26580e3d5ab1.jpg)
![Tercer forma(2)](https://static.platzi.com/media/user_upload/Captura%20de%20Pantalla%202019-04-30%20a%20la%28s%29%2017.27.52-cb96ff88-e8f4-4957-8bbb-ded1cc6cf599.jpg)

- **Cuarta Forma Normal (4FN):** Cumple con las formas normales anteriores y agrega que los campos multivaluados deben ser identificados por una clave única, evitando redundancias en los datos.

![Cuarta forma](https://static.platzi.com/media/user_upload/Captura%20de%20Pantalla%202019-04-30%20a%20la%28s%29%2017.29.00-ba58de30-a08d-472a-82f9-ea478bf6fcee.jpg)
![Cuarta forma(2)](https://static.platzi.com/media/user_upload/Captura%20de%20Pantalla%202019-04-30%20a%20la%28s%29%2017.29.29-149d96f3-78e4-4a26-8c4a-0f002c81cc2f.jpg)

La normalización ayuda a evitar problemas de redundancia, inconsistencia y anormalidad en los datos, lo que conduce a una base de datos más estructurada, eficiente y fácil de mantener. Sin embargo, es importante recordar que, en algunas situaciones, la normalización excesiva puede llevar a la necesidad de realizar un mayor número de uniones en las consultas, lo que puede afectar el rendimiento. 