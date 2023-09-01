


## Instalación local de MySQL

Hay dos maneras de acceder a manejadores de bases de datos:

- Instalar en máquina local un administrador de bases relacional.
- Tener ambientes de desarrollo especiales o servicios cloud.

En este curso usaremos MySQL porque tiene un impacto histórico siendo muy utilizado y además es software libre y gratuito. La versión 5.6.43 es compatible con la mayoría de aplicaciones y frameworks.

***Root es el usuario principal que tendrá todos los permisos y por lo tanto en ambientes de producción hay que tener mucho cuidado al configurarlo.***

1. Visitamos y descargamos el instalador en el sitio web de [MySQL](https://dev.mysql.com/downloads/installer/).

2. Una vez descargado, ejecutar el archivo y seguir las instrucciones en pantalla.

![Pantalla del instalador 1](https://github.com/rb-one/Notas-fundamentos-bases-de-datos/blob/master/Notas/src/Instalador_mysql_1.png?raw=true)

Continúa siguiendo las instrucciones del instalador hasta que se complete la instalación. Asegúrate de leer cuidadosamente cada pantalla y opción para asegurarte de que se configure de acuerdo a tus necesidades.

![Pantalla del instalador 2](https://github.com/rb-one/Notas-fundamentos-bases-de-datos/raw/master/Notas/src/Instalador_mysql_2.png)

Durante la instalación, se te pedirá que configures el servidor MySQL. Esto puede incluir establecer una contraseña para el usuario "root", configurar el modo de autenticación y otros ajustes.

![Pantalla del instalador 3](https://github.com/rb-one/Notas-fundamentos-bases-de-datos/raw/master/Notas/src/Instalador_mysql_3.png)

Una vez que se haya instalado MySQL, puedes abrir una terminal o el administrador de servicios (según tu sistema operativo) para verificar que el servidor MySQL esté en funcionamiento.

### Cliente gráfico

MySQL Workbench proporciona una interfaz visual intuitiva que permite a los usuarios realizar tareas como diseñar y ejecutar consultas, modelar bases de datos, administrar usuarios y mucho más. Es una herramienta esencial para aquellos que trabajan con bases de datos MySQL.

![Primera vista de workbench](https://github.com/rb-one/Notas-fundamentos-bases-de-datos/raw/master/Notas/src/worckbench_1.png)
*Pantalla principal*

![Creación de una Base de datos](https://github.com/rb-one/Notas-fundamentos-bases-de-datos/raw/master/Notas/src/worckbench_2.png)
*Creación de una base de datos*

![Configuracion inicial base de datos](https://github.com/rb-one/Notas-fundamentos-bases-de-datos/raw/master/Notas/src/worckbench_3.png)
*Configuración base de datos*

# Oracle

1. Visitamos y descargamos el instalador en el sitio web de [MySQL](https://www.oracle.com/co/database/technologies/appdev/xe.html).

2. Una vez descargado, ejecutar el archivo y seguir las instrucciones en pantalla.




### sql
spool clase
create table profesores
select * from tab; // Ver las entidades creadas
create table alumnos



## Servicios administrados

Son soluciones en la nube que ofrecen la administración y operación de bases de datos relacionales de manera gestionada por proveedores de servicios en la nube. Estos servicios permiten a las organizaciones externalizar la complejidad de administrar y mantener sus bases de datos, lo que les permite centrarse más en el desarrollo de aplicaciones y en la utilización de los datos en lugar de gestionar la infraestructura subyacente.

Algunos RDBMS populares son:

- Amazon RDS
- Azure SQL Database
- Google Cloud SQL
- Oracle Cloud Database
- IBM Db2 on Cloud

Las ventajas de utilizar servicios administrados de RDBMS incluyen:

- Facilidad de Uso: Los servicios administrados eliminan la necesidad de administrar la infraestructura subyacente, lo que facilita el enfoque en el desarrollo y el uso de datos.

- Elasticidad y Escalabilidad: Estos servicios permiten escalar vertical u horizontalmente según las necesidades sin la necesidad de gestionar servidores.

- Alta Disponibilidad: Muchos de estos servicios ofrecen características de alta disponibilidad y copias de seguridad automáticas.

- Seguridad: Los proveedores suelen implementar medidas de seguridad para proteger los datos almacenados.

- Actualizaciones y Mantenimiento: Los proveedores se encargan de las actualizaciones y mantenimiento del sistema, asegurando que las bases de datos estén actualizadas y funcionando correctamente.

- Reducción de Costos y Tiempo: Al no tener que administrar la infraestructura, las organizaciones pueden ahorrar en costos y tiempo de administración.