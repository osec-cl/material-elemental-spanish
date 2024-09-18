---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
footer: Material OSEC - CC BY-NC-SA
---

# **Computadora**

Introducción al *intérprete de comandos*.
Introducción a la *entrada* y *salida*.
Introducción a la *jerarquía de archivos*.

---

# User Space vs Kernel Space

* El Sistema Operativo administra elementos de la máquina tales como CPU y almacenamiento para proveer servicios.

  * A esto se le conoce como *Kernel Space*.

* Los usuarios del Sistema Operativo hacen uso de estos servicios para llevar a cabo tareas en la máquina.

  * A esto se le conoce como *User Space*.

Para la máquina, estas tareas son instrucciones leídas por el Sistema Operativo mediante el **Intérprete de Comandos**.

---

# Command-line Interpreter

El intérprete de comandos es el programa encargado de comunicar la entrada interactiva por parte de las personas al S.O.

* Se define como *comando* a los programas con instrucciones que el S.O. es capaz de leer y ejecutar.

* Se define como *entrada interactiva* a aquella producto de una interacción externa realizada por una persona.

---

# TTY &ndash; Teletypewriter

La primera entrada interactiva con una computadora consistió en una máquina de escribir eléctrica.

* Cada tecla pulsada es convertida a una secuencia en binario.

* Es una mejora respecto de los telégrafos.

* Cada punto de la comunicación es una computadora.

* La salida se imprime en papel utilizando tinta.

---

# Computer Monitor

Las computadoras dejan de utilizar papel para emitir su salida tras la creación de pantallas que pueden representarla con imágenes.

* Primero pantallas de rayos catódicos (CRT).

* Luego pantallas a base de LED's (LCD).

* En el presente pantallas táctiles y OLED.

---

# Workflow

* *Entrada* interactiva mediante máquina de escribir eléctrica.

  * Esta evoluciona a un teclado dedicado.

* *Sistema Operativo* que administra recursos de la máquina.

  * Este evoluciona a sistemas *UNIX* y *DOS*.

* *Salida* dinámica mediante monitor CTR / LCD / OLED.

  * Nacen los sistemas *headless* o servidores.

---

# UNIX Shell

Los sistemas derivados de UNIX establecen un conjunto de reglas que estructuran la entrada, salida y almacenamiento de la información.

* El intérprete de comandos recibe la entrada.

  * Se denomina *shell* al programa que realiza esta tarea.

* La información se almacena en la *jerarquía de archivos.*

* El interprete de comandos imprime una salida.

  * La salida es intercalada con la entrada en pantalla.

---

# FHS &ndash; Filesystem Hierarchy Standard

El sistema operativo organiza la información manteniendo una jerarquía de archivos dentro del almacenamiento.

* Capa de abstracción provista por el sistema operativo y a la que se puede acceder mediante llamadas al sistema.

* El sistema operativo expone parte de sus servicios dentro de esta jerarquía, enforzando permisos de acceso dentro de ella.

* El intérprete de comandos opera por sobre esta capa de abstracción, asumiendo el sistema de organización.

---

# FHS &ndash; Filesystem Hierarchy Standard

Cada carpeta dentro de la jerarquía es denominada *directorio*, a continuación una suscinta descripción de los más importantes.

* **/bin** &ndash; contiene los programas esenciales del sistema.

* **/boot** &ndash; contiene programas y archivos de configuración que permiten inicializar el S.O. tras encender la computadora.

* **/dev** &ndash; contiene representaciones a unidades de la máquina e.g. teclado, pantalla, almacenamiento reconocidas por el S.O.

---

# FHS &ndash; Filesystem Hierarchy Standard

Cada carpeta dentro de la jerarquía es denominada *directorio*, a continuación una suscinta descripción de los más importantes.

* **/etc** &ndash; contiene archivos de configuración que modifican el comportamiento de los programas.

* **/home** &ndash; contiene los directorios personales de los usuarios de la computadora (en particular personas reales).

* **/lib** &ndash; contiene archivos binarios compartidos entre programas.

---

# FHS &ndash; Filesystem Hierarchy Standard

Cada carpeta dentro de la jerarquía es denominada *directorio*, a continuación una suscinta descripción de los más importantes.

* **/media** &ndash; cada directorio corresponde al contenido de una unidad de almacenamiento presente en */dev* y anexada a la jerarquía.

* **/mnt** &ndash; misma definición que */media*, excepto que estos directorios fueron incluidos manualmente por un usuario y no el S.O.

---

# FHS &ndash; Filesystem Hierarchy Standard

Cada carpeta dentro de la jerarquía es denominada *directorio*, a continuación una suscinta descripción de los más importantes.

* **/opt** &ndash; contiene programas que no pueden ser integrados al resto de la jerarquía por ser privados o requerir una licencia paga.

* **/tmp** &ndash; contiene archivos temporales creados por programas durante su ejecución, su contenido no se conserva.

* **/usr** &ndash; sub-jerarquía donde múltiples programas comparten archivos y que el S.O. utiliza para extender su funcionalidad.

---

# FHS &ndash; Filesystem Hierarchy Standard

A continuación directorios que cumplen labores administrativas dentro del S.O. y son más específicos en su propósito.

* **/proc** &ndash; representaciones de los programas en ejecución del S.O.

* **/root** &ndash; directorio personal especial para el super usuario.

* **/run** &ndash; misma definición que */tmp*  pero más estricta.

* **/var** &ndash; contiene los directorios donde los programas guardan los archivos que generan durante su ejecución.

---

# FHS &ndash; Filesystem Hierarchy Standard

La sub-jerarquía **/usr** es, por definición, de sólo lectura. Contiene todos los programas y archivos requeridos para permitir a múltiples usuarios realizar tareas dentro del sistema operativo.

* **/usr/bin** &ndash; programas no esenciales para la inicialización y administración del sistema operativo.

* **/usr/lib** &ndash; contraparte de */lib* para archivos no esenciales.

* **/usr/share** &ndash; contiene archivos no ejecutables pero que no modifican el comportamiento de los programas (e.g. imágenes).

---

# FHS &ndash; Filesystem Hierarchy Standard

La sub-sub-jerarquía **/usr/local** es una copia de */usr* y tiene como objetivo permitir la instalación de programas que no están integrados con las jerarquías superiores sin afectar el orden del FHS.

Otros directorios que pueden modificarse manualmente son:

* **/usr/src** &ndash; contiene código fuente de programas.

* **/usr/libexec** &ndash; estándar no oficial previo a */lib* y */usr/lib* cuyo objetivo es contener programas auxiliares para otros programas.