---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
footer: Material OSEC - CC BY-NC-SA
---

# **Comandos Disponibles**

Introducción shell *keywords* y shell *builtins*
Introducción a *coreutils*, *findutils* y *diffutils*.

---

# Bash Keywords

Conjunto de palabras pertenecientes al lenguaje de programación de Bash que permiten operar lógica en la shell.

* *for*
* *while*
* *if*
* *elif*
* *else*

---

# Bash builtins

Conjunto de palabras interpretados por la shell como comandos.

* Para imprimir texto en pantalla.

```
$ echo "Soy texto"
```

* Para identificar si *palabra* es un comando, keyword o builtin.

```
$ type palabra
```

---

# coreutils &ndash; Core Utilities

Conjunto de programas básicos disponibles en un sistema Linux para la manipulación de archivos y directorios por parte del usuario.

Un listado breve de ellos es:

* *pwd* - imprime el *Working Directory*
* *ls* - lista el contenido de un directorio.
* *mkdir* - crea un directorio.
* ... entre otros.

---

# findutils &ndash; Find Utilities

Conjunto de programas para buscar archivos en directorios.

Se destacan los comandos:

* *find* - busca archivos en una jerarquía de directorios.
* *xargs* - crea y ejecuta comandos a partir de la entrada estándar.

---

# diffutils &ndash; Difference Utilities

Conjunto de programas para ver la diferencia entre dos archivos.

Se destacan los comandos:

* *cmp* - compara dos archivos byte por byte.
* *diff* - compara dos archivos línea por línea.
* *sdiff* - fusiona la diferencia entre dos archivos.