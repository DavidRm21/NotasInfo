# Oracle

Oracle es una empresa líder en software y servicios relacionados con bases de datos, sistemas de gestión empresarial (ERP), aplicaciones en la nube y tecnología de información. 

- Características

  - Alta disponibilidad
  - Escalabilidad
  - Seguridad avanzada
  - Confiabilidad
  - Integración con otros sistemas y aplicaciones.
  - Amplia comunidad y de soporte 
  - Basado en estandares y con extensiones propietarias (SQL, PL/SQL, Oracle forms/reports, APEX, OBIEE, etc)

  <br>
  <br>

# Fases para el desarrollo de un sistema

## 1. Estrategia y análisis

  - **Identificación de necesidades:** Comprender y documentar las necesidades y requisitos del negocio.
  - **Definición de objetivos:** Establecer metas y objetivos para el sistema que se va a desarrollar.
  - **Análisis de viabilidad:** Viabilidad técnica, financiera y operativa.
  - **Estudio del mercado:** Investigación de competencia y tendencias en el mercado.
  - **Planificación del proyecto:** Definir el alcance, el cronograma, el presupuesto, y los recursos necesarios.

  <br>

## 2. Diseño

  - **Definir la estructura general:** Componentes principales y relaciones.
  - **Diseño de la interfaz de usuario:** Creación de prototipos y diseños de interfaz que los usuarios interectuarán.
  - **Diseño de la base de datos**
  - **Diseño detallado** (Caso de uso)

  <br>

## 3. Construcción y documentación

  - **Desarrollo de software:** Escribir el código fuente del sistema a partir de los diseños y especificaciones.
  - **Pruebas:** Realizar pruebas unitarias y de integración para verificar su funcionamiento.
  - **Documentación:** Crear documentación técnica y de usuario para el sistema.

  <br>

## 4. Transición

  - **Pruebas de aceptación:** Asegurarse de que el sistema cumpla con las necesidades.
  - **Capacitación:** de los usuarios y el personal de soporte.
  - **Migración de datos:** Transferencia del sistema antiguo a uno más actual, en caso de que aplique.
  - **Preparación para la puesta en marcha:** Asegurarse que todos los recursos y procesos esten listos para la implementación.

  <br>

## 5. Producción

  - **Implentación:** Lanzar el sistema a producción.
  - **Monitoreo y mantenimiento:** Supervisar el sistema en funcionamiento, realizar ajustes y correcciones.

  <br>

El desarrollo de sistemas es un proceso iterativo, a lo largo de las fases es posible que se deban realizar revisiones y ajustes en función de las retroalimentaciones y cambios en los requisitos del cliente.

  <br>
  <br>

<details>
  <summary><b> Preguntando a la base de datos 🤔❔</b></summary>

```sql
SELECT -- Lo que quiero mostrar

FROM -- De dónde voy a tomar los datos (tablas unicas o con joins)

WHERE -- Los filtros de los datos que quiero mostrar

GROUP BY -- Los rubros por los que me interesa agrupar la información

ORDER BY -- El orden en que quiero presentar mi información

HAVING -- Los filtros que quiero que mis datos agrupados tengan
```

</details>

<details>
  <summary><b>Exportar e importar mi base de datos Oracle 💾 </b></summary>

<br>
<hr>

**Exportar una base de datos con Oracle.**

1. Abre una ventana de línea de comandos en el servidor de datos o en una máquina cliente con Oracle Instant Client instalado.

2. Inicia sesión como un usuario con privilegios adecuados, como el usuario "SYSDBA" o un usuario con el privilegio "DBA".

3. Ejecuta el comando "exp" para exportar la base de datos.

```sql
host exp userName/password owner=userName file=nombreArchivo.dmp

--- Ejemplo
host exp Wazowski/123456 owner=Wazowski file=MiBaseDeDatos.dmp
```

Este archivo se guardará en la ruta:

> C:\orant\BIN

<br>

**Importar una base de datos Oracle**

El archivo resultante de la exportación debe ser copiado a la siguiente ruta:

> C:\orant\BIN

1. Abre una ventana de línea de comandos en el servidor de la base de datos o en una máquina cliente con Oracle Instant Client instalado.

2. Inicia sesión como un usuario con privilegios adecuados, como el usuario "SYSDBA" o un usuario con el privilegio "DBA".

3. Ejecuta el comando "imp" para importar la base de datos.

```sql
host imp  userName/password fromuser=userName file=DataBase.dmp  touser=userName;

--- Ejemplo
host imp Wazowski/123456 fromuser=Wazowski file=MiBaseDeDatos.dmp touser=Sullivan;
```



- **userName/password**: Las credenciales del usuario de la base de datos con permisos para realizar la exportación e importación.
- **fromuser**: Esto indica que estás importando datos desde un esquema o propietario específico.
- **file**: El nombre del archivo de volcado (dump) que contendrá los datos exportados.
- **touser**: Indica que los datos se importarán al esquema de usuario especificado.

</details>


<br>
<br>

# **SQL**

SQL (Structured Query Language) es un lenguaje de consulta estructurado utilizado para administrar y manipular bases de datos relacionales. Tiene una estructura definida y su objetivo principal es proporcionar una forma estándar y coherente para interactuar con sistemas de gestión de bases de datos relacionales.

# **SQL tiene contiene 4 sublenguajes**

<br>

<details>
  <summary><b> DDL </b></summary>

(Data Definition Language) se utiliza para definir y administrar la estructura y el esquema de una base de datos. 

Los comandos DDL más comunes son:

- **CREATE:** Se utiliza para crear objetos de la base de datos, como tablas, índices, vistas, funciones almacenadas y procedimientos almacenados.

- **ALTER** Permite modificar la estructura de los objetos de la base de datos existentes, como añadir o eliminar columnas de una tabla, modificar el tipo de datos de una columna o cambiar el nombre de un objeto.
- **DROP** Se utiliza para eliminar permanentemente objetos de la base de datos, como tablas, vistas, índices, funciones almacenadas, entre otros.
- **TRUNCATE** Permite eliminar todos los datos de una tabla, manteniendo la estructura de la tabla intacta.
- **RENAME** Permite cambiar el nombre de un objeto de la base de datos, como una tabla o una columna.
- **CONSTRAINT** Se utiliza para definir restricciones en las tablas, como claves primarias, claves foráneas, restricciones de integridad, entre otros.
- **GRANT y REVOKE** Estos comandos se utilizan para otorgar o revocar permisos de acceso a los objetos de la base de datos.

![Objetos en DDL](https://github.com/rb-one/Notas-fundamentos-bases-de-datos/raw/master/Notas/src/SQL_create.png)

*Los 3 objetos que manipulamos con DDL*

</details>
<details>
  <summary><b> DML </b></summary>
(Data Manipulation Language) se utiliza para manipular y operar sobre los datos almacenados en una base de datos. 

Los comandos DML más comunes son:

- **SELECT**: Se utiliza para recuperar datos de una o varias tablas en la base de datos.

- **INSERT**: Permite insertar nuevos registros en una tabla de la base de datos. 

- **UPDATE**: Se utiliza para modificar los datos existentes en una o varias filas de una tabla. 

- **DELETE**: Permite eliminar uno o varios registros de una tabla en la base de datos. 

</details>

</details>
<details>
  <summary><b> DCL </b></summary>
(Data Control Language) se utiliza para controlar los permisos de acceso y la seguridad en una base de datos.

- **GRANT**: Se utiliza para otorgar privilegios y permisos de acceso a los usuarios sobre los objetos de la base de datos. *Leer, escribir, modificar o eliminar* datos en tablas.

- **REVOKE**: Permite revocar o retirar los privilegios y permisos otorgados previamente a los usuarios.

- **DENY**: Permite negar explícitamente ciertos privilegios a los usuarios.

</details>

</details>
<details>
  <summary><b> TCL </b></summary>
(Transaction Control Language) Son utilizados para gestionar y controlar transacciones en una base de datos. 

Los comandos más comunes son:

- **COMMIT**: Se utiliza para confirmar una transacción y aplicar permanentemente los cambios realizados en la base de datos.

- **ROLLBACK**: Permite deshacer una transacción en su totalidad, descartando todos los cambios realizados.

- **SAVEPOINT**: Se utiliza para establecer puntos de control dentro de una transacción, lo que permite deshacer solo una parte de la transacción hasta un punto específico.
</details>

<br>
<br>


# Comandos

### spool y commit

Al ingresar a la terminal de OracleSQL PLus, debemos ingresar el comando spool para capturar y guardar los resultados de consultas SQL u otro mensaje que se desee conservar.

```sql
SQL> -- Para comenzar a capturar la salida en un archivo:
SQL> SPOOL nombreDelArchivo

SQL> -- Ejecuta tus consultas y lógica en esta sesión...
SQL> SELECT * FROM mi_tabla;
SQL> COMMIT;  -- Guarda cambios si es necesario

SQL> -- Para detener la captura y cerrar el archivo de registro:
SQL> SPOOL OFF
```

Este archivo se guardará en la ubicación predeterminada:

> C:\orant\BIN\nombreDelArchivo.LST

### ed 

Es una abreviatura de "EDIT" y se utiliza para editar o crear un nuevo comando SQL o PL/SQL en un editor de texto externo.

Después de ejecutar el comando `ed`, se abrirá un editor de texto en la pantalla que te permite modificar la instrucción que estás trabajando. Para salir del editor de texto, simplemente ve al menú "Archivo", guarda los cambios y luego selecciona la opción "Salir". Para ejecutar lo que has editado, regresa a la terminal, coloca un "/" (barra inclinada) y presiona la tecla Enter.

```sql
SQL> /
```

### Tipos de datos

VARCHAR2

```sql
-- Tiene ventajas a comparación del VARCHAR
```

NUMBER

```SQL
-- Puede ser decimal y entero
-- Tiene mayor capacidad de almacenamiento
```

DATE

```SQL
'2017-11-23'
'12-NOV-2023'
```
TIMESTAMP

```sql
'2017-11-24 08:45:41.434175'
```

# [Consultas SQL](./3_SQL-MySQL.md) 

# Operadores en Oracle Database

### 1. Operadores Aritméticos (+ - / *)

<details>
<summary><b>Tabla de prueba</b></summary>

```sql
CREATE TABLE TB_NOTAS_ALUMNOS (
  cod_al NUMBER PRIMARY KEY,
  nombre_al VARCHAR2 NOT NULL,
  curso VARCHAR2,
  nota1 NUMBER DEFAULT 0,
  nota2 NUMBER DEFAULT 0,
  nota3 NUMBER DEFAULT 0,
  promedio NUMBER DEFAULT 0 
);

INSERT INTO TB_NOTAS_ALUMNOS VALUES (1, 'Carlos', 'Matematicas', 45, 30, 42, 0);
INSERT INTO TB_NOTAS_ALUMNOS VALUES (2, 'Elena', 'Matematicas', 35, 25, 40, 0)
INSERT INTO TB_NOTAS_ALUMNOS VALUES (3, 'Linda', 'Fisica', 45, 40, 42, 0)
INSERT INTO TB_NOTAS_ALUMNOS VALUES (4, 'Matias', 'Quimica', 42, 38, 32, 0)
```
</details>

***Suma de valores***

```sql
SELECT cod_al, nombre_al, (nota1+nota2+nota3) "Sumatoria_notas" FROM TB_NOTAS_ALUMNOS;
```

| cod_al  |  nombre_al | Sumatoria_notas  
|---|---|---|
| 1 | Carlos  | 117  |
| 2 | Elena  | 100  |
| 3 | Linda  | 127  |
| 4 | Matias  |  112 |

***Resta de valores***

```sql
SELECT cod_al, nombre_al, (nota1+nota2) "Acumulado_notas1y2", nota3, (nota1+nota2)-nota3 "Nota1y2Menos3"  
FROM TB_NOTAS_ALUMNOS;
```

| cod_al  |  nombre_al | Acumulado_notas1y2 | nota3 |  Nota1y2Menos3 | 
|---|---|---|---|---|
| 1 | Carlos  | 75  | 42 | 33 |
| 2 | Elena  | 60  | 40 | 20 |
| 3 | Linda  | 85  | 42 | 43 |
| 4 | Matias  |  80 | 32 | 48 |

**Multiplicación de valores**

```sql
SELECT cod_al, nombre_al, (nota1*nota2) "Mult_Nota1y2"
FROM TB_NOTAS_ALUMNOS;
```

| cod_al  |  nombre_al | Mult_Nota1y2  
|---|---|---|
| 1 | Carlos  | 1350  |
| 2 | Elena  | 875  |
| 3 | Linda  | 1800  |
| 4 | Matias  |  1596 |

***División de valores***

La función *ROUND* nos ayuda a redondear un valor decimal en este caso solo quiero que me muestre dos decimales despues de la coma.

```sql
SELECT cod_al, nombre_al, curso, ROUND(((nota1+nota2+nota3)/3),2) "promedio"
FROM TB_NOTAS_ALUMNOS;
```

| cod_al  |  nombre_al | curso | promedio | 
|---|---|---|---|---|
| 1 | Carlos  | Matematicas  | 39 |
| 2 | Elena  | Matematicas  | 33,33 |
| 3 | Linda  | Fisica  | 42,33 |
| 4 | Matias  |  Quimica | 37,33 |



### 2. Operadores relaciones o de comparación

### 3. Operadores de concatenación

### 4. Operadores lógicos