---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
footer: Material OSEC - CC BY-NC-SA
---

# **Sistema**

Introducción a *PATH* y *Working Directory*.
Introducción al árbol de directorios.
Introducción a *rutas* y *dotfiles*.

---

# PATH

El FHS es la estructura abstracta con la que se interactúa mediante el intérprete de comandos. No obstante, este programa (*la shell*) sólo es capaz de ejecutar otros programas (*los comandos*) para sus tareas.

* La noción de *PATH* corresponde a la colección de todos los programas ejecutables dentro de la jerarquía de archivos.

* **/usr/local/bin:/usr/bin:/bin**

  * El '**:**' es un separador. La shell busca de izquierda a derecha en PATH cada programa que se le solicita ejecutar.

---

# Working Directory

La shell se ubica en algún punto del FHS, desde el momento en que se ejecuta hasta el momento en que termina su ejecución.

* El directorio de trabajo es la ubicación de la shell dentro del FHS.

* El directorio de trabajo sólo puede cambiarse manualmente.

* Tantos la shell como el resto de los programas pueden condicionar su comportamiento conforme al directorio de trabajo actual.



---

# Árbol de directorios

La jerarquía de archivos corresponde a un árbol donde cada nodo interno es un directorio y cada nodo externo o terminal un archivo.

* Se encuentra presente en todos los sistemas *UNIX*.

* El árbol comienza en `/`, el directorio raíz.

* Cada archivo o directorio conforma una *ruta* con respecto al directorio raíz y siempre mantiene una relación con el árbol.

  * No puede haber archivos o directorios sin una ruta de regreso a la raíz, sin importar si están en otro dispositivo o máquina.

---

# Absolute Path

Una ruta absoluta comienza en la raíz del árbol de directorios (`/`) y termina en el archivo o directorio objetivo.

Algunos ejemplos:

* **/usr/local/bin/myprogram**
  * Una ruta abosulta al programa *myprogram*.

* **/dev/eth0**
  * Una ruta absoluta al adaptador de internet *eth0*.

---

# Relative Path

Una ruta relativa no comienza con `/` y utiliza como raíz al directorio de trabajo. La shell concatena ambas  para obtener la ruta absoluta.

Algunos ejemplos:

* Si el directorio de trabajo es **/usr/local**
  * ... ruta relativa **mydir**
  * ... corresponde a la ruta absoluta **/usr/local/mydir**

---

# Path vs *Ruta*

En inglés las rutas son referidas como *paths*, mas no deben confundirse con la palabra en mayúsculas *PATH*.

* Un *absoulte path* empieza en la raíz del árbol.

* Un *relative path* empieza en el *working directory*.

* Un *PATH* es una colección de *absolute paths* que contienen programas ejecutables por la shell.

* Una ruta puede llevar a un archivo o a un directorio.

---

# Archivos punto (dotfiles)

* Archivos o directorios cuyo nombre empieza con `.`.

* Excluyen a `.` (punto) y `..` (doble punto).

* Comunmente utilizados dentro de `/home`.

* Tanto la shell como otros progrmamas los ignoran.

* Son utilizados para guardar configuración de programas.

---

# Directorios reservados

Cada directorio reserva en su interior dos nombres:

* `.` (punto) - referencia al *Working Directory*.

  * La ruta **/usr/local/.**
    * Corresponde a */usr/local*

* `..` (doble punto) - referencia al directorio superior.

  * La ruta **/usr/local/..**
    * Corresponde a */usr*

---

# XDG Base Directory Specification

Directorios reservados para configuraciones de programas.

  * Se utilizan únicamente dentro de `/home`.

    * `.local` - archivos creados por programas.

    * `.config` - archivos de configuración de programas.

    * `.cache` - archivos con información que puede prescindirse.