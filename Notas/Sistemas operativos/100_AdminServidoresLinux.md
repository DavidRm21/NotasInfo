###### Recursos de "Curso de instroduccón a la administración de servidores Linux - Platzi"

# Habilidades y roles de un administrador Linux

## Habilidades

- **Control de accesos:** Otorgar privilegios a usuarios o grupos de usuarios para que pueden acceder al sistema.

- **Monitoreo del sistema:** Saber quien entra al sistema, cuando lo hace, incluso conoce los recursos que utiliza tanto a nivel de hardware como de software.

- **Administración de recursos:** Saber cuanta memoria debe asignarse a ciertos procesos.

- **Troubleshooting:** Capacidad para resolver problemas.

- **Instalación y mantenimiento de software**

- **Creación de respaldos**

- **Documentación**

## Roles

- DevOps Enginner

- Site Reliability Engineer

- Security Operations Engineer

- Network Engineer

- Database Administrator

- Cloud Engineer

- Tech support engineer

- Network Security Analyst

- IT project manager (con background e SysAdmin claro)

- Storage Admin

- App Dev engineers

<br>
<br>
<br>

# ¿Qué son los servidores?

Es un grupo de recursos tecnológicos (hardware y software) que cumplen con uno o varios propósitos.

Usualmente peticiones de un cliente y luego otorgan una respuesta

## Tipos de servidores

- Web (fronted y backend)

- Bases de datos

- De pruebas

- Videojuegos

- Medios

- Email

- Impresión 

- Archivos y recursos (SFTP, SMB)

- VoIP

---

# ¿Qué es un sistema Linux / UNIX

Linux en un kernel, una parte del sistema operativo sobre el cual se ejecutan otros programas de acuerdo a la necesidad del usuario. Es de software libre, lo que quiere decir que cualquiera puede personalizar y generar distribuciones de esté (Ubuntu, RedHat, Centos, Fedora, OpenSuse, Debian, etc)

GNU/Linux es una familia de sistemas operativos que usan a linux como kernel y una gran coleccion de programas para conformar un sistema operativo completo.

### ¿Cual es la diferencia entre Linux y UNIX?

Unix es un sistema operativo desarrollado en el año 1969 por los laboratorios Bell de AT&T.

Linux se inspiró en los principios de UNIX, son dos sistemas operativos distintos en términos de licencia, desarrollo, distribuciones y enfoques de comunidad y soporte. Linux es conocido por su naturaleza de código abierto, su amplia variedad de distribuciones y su comunidad activa, mientras que UNIX tiende a ser más comercial y propietario en su enfoque.

## Arquitectura de un sistema UNIX/Linux

- Hardware: Son todos los dispositivos E/S.

- Kernel: Es la parte clave de todo sistema operativo Linux. Nos permite controlar todo el hardware de nuestro servidor como el uso de CPU o memoria RAM.

- Shell: Es la interfaz entre el kernel y el usuario, es quien nos permite ejecutar comandos y pasarlos a un sistema de bajo nivel.

- Utilidades y aplicaciones: Es donde el usuario interactúa directamente. Es la capa donde trabajan todos nuestros comandos y aplicaciones.

<br>

# Breve historia del software libre y el open source

Richard Stallman tuvo un problema con las impresoras XEROX debido a que sus impresoras venian con una fallo a la hora de aplicar concurrencia, él habia creado un pedazo de código para resolver la cola de impresión, pero al tratar de que la compañia arreglará el fallo obtuvo una respuesta negativa por lo que él mismo creo un sistema operativo llamado GNU que podia destapar el código fuente y cambiar cualquier código. Luego fundo la compañia Free Software Foundation en 1985 y establece las cuatro libertades que puede tener un software libre:

- La libertad de ejecutar

- La libertad de estudiar el funcionamiento del programa y modificarlo.

- La libertad de redistribuir.

- La libertad de distribuir copias de sus versiones modificadas a otras personas.

- Utiliza licencias GPL, LGPL, BSD, MIT, Apache, etc.

En otro lado del mundo, un joven llamado Linus Torvalds comparte por primera vez el proyecto de Linux que tenia similitud con UNIX en 1993 se convierte en software libre, y es utilizado a todos los sistemas operativos basados en Linux.

En los años 90 nace la iniciativa Open Source:

- El código fuente esta disponible publicamente y puede ser examinado, modificado.

- No suele tener libertad de redistribuir o cobrar por él.

- Se centra en la colaboración y la revisión del código fuente para mejorar y hacer avanzar el software.

- El desarrollo puede ser realizado tanto por una comunidad como por una empresa privada

- Fomenta la innovación y el avance del software al permitir que un gran número de personas colaboren y contribuyan al proyecto

- Utiliza licencias como Apache, BSD, MIT, etc.

La diferencia entre sofware libre y el Open Source es su filosofia y libertades. 

# Sistemas operativos y distribuciones

Una distribución interpreta el Kernel de Linux, puede variar en el formato, manejador de paquetes y popularidad.

Los sistemas operativos más populares son:

- RedHat Enterprise Linux

- Ubuntu Server

- FreeBSD

- Debian


# ¿Donde se alojan los servidore?

## On premise

Todo el hardware y software del servidor es alojado y mantenido por la organización.

## Cloud

Todo el hardware y en parte el software es alojado y mantenido por una compañia en algún lugar remoto, sólo se encarga de administrar los recursos.

##  Hybrid

Es una combinación entre On premise y Cloud

# Formas de instalar

## Instalación directa

Se instala un sistema operativo para ocupar el 100% de los recursos dedicados ya sea a un solo servicio o varios.

## Virtualización

Se instala un software que sirve como host conocido como (hypervisor) que administra los recursos para crear multiples guests.

## Hypervisor (Virtual box) 

- Tipo 1 (Bare Metal): No necesita un sistema operativo para funcionar.

- Tipo 2 (Hosted): Requiere un host como sistema operativo.

## Contenedores

- Los contenedores son excelentes para implementaciones a gran escala y para aplicaciones que se benefician de un inicio rápido y un uso eficiente de recursos. 

## Maquinas virtuales

- Las VMs son ideales cuando se necesita ejecutar diferentes sistemas operativos o cuando se requiere un alto nivel de aislamiento.
