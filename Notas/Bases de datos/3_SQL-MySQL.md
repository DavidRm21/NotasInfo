# [¿Cómo hacer consultas SQL? 😎](#¿cómo-hacer-consultas-sql)


# **SQL**

SQL (Structured Query Language) es un lenguaje de consulta estructurado utilizado para administrar y manipular bases de datos relacionales. Tiene una estructura definida y su objetivo principal es proporcionar una forma estándar y coherente para interactuar con sistemas de gestión de bases de datos relacionales.

# **SQL tiene contiene 4 sublenguajes**

<br>

## **DDL**
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

<br>
<br>

## **DML**
(Data Manipulation Language) se utiliza para manipular y operar sobre los datos almacenados en una base de datos. 

Los comandos DML más comunes son:

- **SELECT**: Se utiliza para recuperar datos de una o varias tablas en la base de datos.

- **INSERT**: Permite insertar nuevos registros en una tabla de la base de datos. 

- **UPDATE**: Se utiliza para modificar los datos existentes en una o varias filas de una tabla. 

- **DELETE**: Permite eliminar uno o varios registros de una tabla en la base de datos. 

<br>
<br>

## **DCL**
(Data Control Language) se utiliza para controlar los permisos de acceso y la seguridad en una base de datos.

- **GRANT**: Se utiliza para otorgar privilegios y permisos de acceso a los usuarios sobre los objetos de la base de datos. *Leer, escribir, modificar o eliminar* datos en tablas.

- **REVOKE**: Permite revocar o retirar los privilegios y permisos otorgados previamente a los usuarios.

- **DENY**: Permite negar explícitamente ciertos privilegios a los usuarios.

<br>
<br>

## **TCL**
(Transaction Control Language) Son utilizados para gestionar y controlar transacciones en una base de datos. 

Los comandos más comunes son:

- **COMMIT**: Se utiliza para confirmar una transacción y aplicar permanentemente los cambios realizados en la base de datos.

- **ROLLBACK**: Permite deshacer una transacción en su totalidad, descartando todos los cambios realizados.

- **SAVEPOINT**: Se utiliza para establecer puntos de control dentro de una transacción, lo que permite deshacer solo una parte de la transacción hasta un punto específico. 

<br>
<br>

# **Consultas SQL**

---

<details>
  <summary><b> ✔️ Recomendaciones antes de empezar con las consultas</b></summary>

1. Utiliza nombres que sean claros y concisos para facilitar la comprensión.

2. Evitar caracteres especiales.

3. Decide si utilizarás nombres en singular o en plural para las tablas y mantenlo consistente en todo el esquema de la base de datos. 

4. Convenciones de formato (nombreTabla, NombreTable, Nombre_Tabla, nombre_tabla)

5. Evitar palabras reservadas.

</details>

---

<br>
<br>

### **Pasos para crear una base de datos**
---

#### 1. ***Con está sentencia creamos la base de datos***

```sql
CREATE DATABASE nombreBaseDeDatos;
```

#### 2. ***Le indicamos al lenguaje que base de datos vamos a modificar***

```sql
USE nombreBaseDeDatos;
```

#### 3. ***En este ejemplo crearemos dos tablas y una llave foránea***



```sql
CREATE TABLE nombreDeLaTabla  (   
    id_tabla INT(50) PRIMARY KEY AUTO_INCREMENT,
    atributo1 VARCHAR(40) NOT NULL,
    atributo2 VARCHAR(60),
    atributo3 VARCHAR(255) NOT NULL UNIQUE,
    atributo4 INT(50) CHECK (atributo4 >= 18)
);

CREATE TABLE nombreDeLaTabla2  (   
    id_tabla2 INT(50) PRIMARY KEY AUTO_INCREMENT,
    atributo1 VARCHAR(40) NOT NULL,
    atributo2 VARCHAR(60) DEFAULT 'Desconocido',
    atributo3 VARCHAR(255) NOT NULL UNIQUE,
    atributo4 VARCHAR(30),
    FKatributo INT(50) NOT NULL,
    FOREIGN KEY (FKatributo) REFERENCES nombreDeLaTabla(id_tabla)
); 
``` 


<br>

***

🔵 ***Añadir una columna adicional en una tabla.*** 

```sql
ALTER TABLE nombreDeLaTabla
ADD nombreDeLaColumna tipoDato; 
```

***

🔵 ***Renombrar una columna en una tabla.***

```sql
ALTER TABLE nombreDeLaTabla
RENAME COLUMN nombreDeLaColumna TO nuevoNombre;
```

***

🔵 ***Añade una llave foranea a una columna en una tabla.***

```sql
ALTER TABLE nombreDeLaTabla
ADD FOREIGN KEY (nombreColumnaActual) REFERENCES nombreDeLaTabla2(PRIMARY KEY) ;
```

***

### 💾 ***Guardará la base de datos en un terminal o dispositivo de almacenamiento.*** 

```sql
BACKUP DATABASE nombreBaseDeDatos
TO DISK = 'filepath';
```

***

<br>
<br>

❗ ***Eliminar una columna adicional en una tabla.***

```sql
ALTER TABLE nombreDeLaTabla
DROP COLUMN nombreDeLaColumna;
```

***

❗ ***Esta nos eliminará permanentemente la tabla definida***
 ```sql
DROP TABLE nombreDeLaTabla;
```

***

⛔ ***Eliminará permanentemente la base de datos***
 ```sql 
DROP DATABASE nombreBaseDeDatos;
 ```


# 😁 [Base de datos previamente creada](./BaseDatos.md)

## ¿Cómo hacer consultas SQL?

### SELECT:
La sentencia SELECT se utiliza para recuperar datos de una base de datos. Permite seleccionar y mostrar información específica de una o varias tablas, y puede incluir condiciones para filtrar los resultados.

```sql
SELECT*
FROM posts
WHERE fecha_publicacion < '2024'
```

La sentencia SELECT en SQL tiene varias funciones y cláusulas que permiten realizar consultas y manipulaciones avanzadas de datos en una base de datos. Algunos de ellos son:

- **Funciones de agregación:**

    - SUM(): Calcula la suma de valores en una columna.
    - AVG(): Calcula el promedio de valores en una columna.
    - COUNT(): Cuenta el número de filas que cumplen una condición.
    - MIN(): Encuentra el valor mínimo en una columna.
    - MAX(): Encuentra el valor máximo en una columna.

```sql
SELECT COUNT(*) AS numero_post
FROM posts;
```

- **Funciones de texto:**

    - CONCAT(): Combina valores de texto.
    - UPPER(): Convierte texto a mayúsculas.
    - LOWER(): Convierte texto a minúsculas.
    - SUBSTRING(): Obtiene una parte de un valor de texto.
    - LENGTH(): Obtiene la longitud de un valor de texto.

- **Funciones de fecha y hora:**

    - NOW(): Obtiene la fecha y hora actual.
    - DATEPART(): Obtiene partes específicas de una fecha/hora.
    - DATEADD(): Agrega una cantidad específica a una fecha/hora.

- **Clausula [WHERE](#where)**: Permite filtrar los resultados de la consulta según una o más condiciones especificadas.

- **Clausula [GROUP BY](#group-by)**: Se utiliza junto con funciones de agregación para agrupar filas que comparten valores en una o más columnas.

- **Clausula [HAVING](#order-by-y-having)**: Se utiliza con GROUP BY para filtrar los resultados después de aplicar funciones de agregación.

- **Clausula [ORDER BY](#order-by-y-having)**: Ordena los resultados de la consulta en función de una o más columnas en orden ascendente o descendente.

- **Clausula DISTINCT**: Elimina filas duplicadas de los resultados de la consulta.

Puedes asignar un alias con la palabra reservada AS a una columna, tabla y en funciones de agregación para cambiar su nombre en el resultado de la consulta.

```sql
SELECT titulo, fecha_publicacion AS publicado_en, estatus  AS estado
FROM posts;
```
***

### FROM

La cláusula "FROM" se utiliza en una sentencia SELECT para indicar de qué tabla o tablas se van a recuperar los datos. La cláusula "FROM" especifica las fuentes de datos de las cuales se obtendrán los registros que cumplen las condiciones definidas en la consulta.

La sentencia que acompaña a esta consulta es JOIN, se utiliza para combinar datos de varias tablas en función de una condición de coincidencia. Hay diferentes tipos de JOIN, como INNER JOIN, LEFT JOIN, RIGHT JOIN y FULL JOIN, que controlan cómo se combinan las filas de las tablas. 

![SQL Joins](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fscientistcafe.com%2Fnotes%2Fsql%2Fimages%2Fjoindiagram.png&f=1&nofb=1&ipt=620a593a312708fd03de1883b63af60432fc35442554be52eb3c8e6bf6344840&ipo=images)

#### Left Join

```sql
SELECT *
FROM usuarios
    LEFT JOIN posts ON usuarios.id = posts.usuario_id;
```

#### Left join sin interseccion

```sql
SELECT *
FROM usuarios
    LEFT JOIN posts ON usuarios.id = posts.usuario_id
WHERE posts.usuario_id IS NULL;
```

#### Right Join sin intersección

```sql
SELECT *
FROM usuarios
    RIGHT JOIN posts ON usuarios.id = posts.usuario_id
WHERE posts.usuario_id IS NULL;
```

#### Inner Join

```sql
SELECT *
FROM usuarios
    INNER JOIN posts ON usuarios.id = posts.usuario_id;
```

#### Full Join

```sql
SELECT *
FROM usuarios
    LEFT JOIN posts ON usuarios.id = posts.usuario_id

UNION

SELECT *
FROM usuarios
    RIGHT JOIN posts ON usuarios.id = posts.usuario_id;
```

#### Diferencia asimétrica

```sql
SELECT *
FROM usuarios
    LEFT JOIN posts ON usuarios.id = posts.usuario_id
WHERE posts.usuario_id IS NULL

UNION

SELECT *
FROM usuarios
    RIGHT JOIN posts ON usuarios.id = posts.usuario_id
WHERE posts.usuario_id IS NULL;
```
***

### WHERE

Se utiliza en una sentencia SELECT para filtrar los resultados de la consulta según una o más condiciones especificadas.

Algunas funciones y cláusulas que se pueden utilizar con la cláusula "WHERE" son las siguientes:

- **Operadores de comparación**

    - '=' Igual

    - '<' / '<=' Menor que / Menor o igual

    - '>' / '>=' Mayor que / Mayor o igual

    - '<>' Diferente

```sql
SELECT *
FROM posts
WHERE id <= 10 ;
```

```sql
SELECT *
FROM posts
WHERE estatus != 'activo' ;
```

- **Operadores Lógicos**

    - AND

    - OR

    - NOT

- **Operadores de rango**

    - BETWEEN: especificar un rango de valores. 

```sql
SELECT *
FROM posts
WHERE fecha_publicacion BETWEEN "2025-01-01" AND "2025-12-31";
```

```sql
SELECT *
FROM posts
WHERE id BETWEEN 5 AND 10;
```

- **IN y NOT IN**: Puedes utilizar "IN" para buscar valores que coincidan con uno de los valores especificados en una lista y "NOT IN" para excluir esos valores. 

- **LIKE**: Puedes utilizar "LIKE" junto con comodines "%" (cualquier cantidad de caracteres) y "_" (un único carácter) para buscar patrones en valores de texto. 

```sql
-- Todos los post con la palabra escandalo
SELECT *
FROM posts
WHERE titulo LIKE '%escandalo%' ;
```

```sql
-- Todos los post que inicien con la palabra escandalo
SELECT *
FROM posts
WHERE titulo LIKE 'escandalo%' ;
```

```sql
-- Todos los post que terminen con la palabra roja
SELECT *
FROM posts
WHERE titulo LIKE '%roja' ;
```

- **IS NULL o IS NOT NULL**: Utiliza "IS NULL" para encontrar registros con valores nulos en una columna y "IS NOT NULL" para encontrar registros con valores no nulos.

```sql
SELECT *
FROM posts
WHERE usuario_id IS NULL;
;
```

```sql
SELECT *
FROM posts
WHERE usuario_id IS NOT NULL
 AND estatus ='activo'
    AND id < 20
    AND categoria_id = 2
 AND year(fecha_publicacion) = '2025'
;

```

- **Subconsultas**: Puedes usar subconsultas en la cláusula "WHERE" para comparar valores en una subconsulta con valores en la consulta principal. 

***

### GROUP BY

Se utiliza para agrupar filas de una tabla según los valores de una o más columnas. Esta cláusula es comúnmente utilizada junto con funciones de agregación para calcular resúmenes o totales sobre los grupos de datos resultantes.

```sql
-- Agrupado por año
SELECT YEAR(fecha_publicacion) AS post_year, COUNT(*) AS post_quantity
FROM posts
GROUP BY post_year
;
```
```sql
-- Agrupado por mes y estatus
SELECT estatus, MONTHNAME(fecha_publicacion) AS post_month, COUNT(*) AS post_quantity
FROM posts
GROUP BY estatus, post_month 
;
```

***

### ORDER BY y HAVING

La cláusula "ORDER BY" se utiliza para ordenar los resultados de una consulta en función de una o más columnas. Puedes ordenar los resultados en orden ascendente (ASC) o descendente (DESC). Por defecto, el orden es ascendente si no se especifica lo contrario.  

Pueden utilizarse junto a:

- **ASC:** Orden de forma ascendente (por defecto)

```sql
SELECT *
FROM posts
ORDER BY fecha_publicacion
;
```

- **DESC:** Orden de forma descendente.

```sql
SELECT *
FROM posts
ORDER BY fecha_publicacion DESC
;
```

- **LIMIT:** Limita la cantidad de resultados que arroja la consulta.

```sql
SELECT *
FROM posts
ORDER BY fecha_publicacion ASC
LIMIT 5
;
```

- **HAVING:** La cláusula "HAVING" se utiliza junto con "GROUP BY" para filtrar los resultados después de aplicar funciones de agregación. Permite establecer condiciones para los grupos resultantes.

```sql
SELECT MONTHNAME(fecha_publicacion) AS post_month, estatus, COUNT(*) AS post_quantity
FROM posts
GROUP BY estatus, post_month
HAVING post_quantity > 1
ORDER BY post_month
;
```

<br>
<br>

***

## Nested Queries

Las "nested queries" (consultas anidadas), también conocidas como "subqueries" (subconsultas), son consultas SQL que se encuentran dentro de otra consulta principal. En otras palabras, una consulta anidada se utiliza como parte de la condición o el resultado de otra consulta más grande. Las subconsultas son una herramienta poderosa en SQL para realizar operaciones más complejas y avanzadas.

```sql
SELECT new_table_projection.date, COUNT(*) AS posts_count
    FROM (
        SELECT DATE(MIN(fecha_publicacion)) AS date, year(fecha_publicacion) AS post_year
        FROM posts
        GROUP BY post_year
        ) AS new_table_projection
GROUP BY new_table_projection.date
ORDER BY new_table_projection.date
```

***

## Preguntando a la base de datos 🤔

```sql
SELECT -- Lo que quiero mostrar

FROM -- De dónde voy a tomar los datos (tablas unicas o con joins)

WHERE -- Los filtros de los datos que quiero mostrar

GROUP BY -- Los rubros por los que me interesa agrupar la información

ORDER BY -- El orden en que quiero presentar mi información

HAVING -- Los filtros que quiero que mis datos agrupados tengan
```




