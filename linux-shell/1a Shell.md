---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
footer: Material OSEC - CC BY-NC-SA
---

# **Intérprete de Comandos**

Introducción a *Bash*.
Reconocer elementos en una *shell*.

---

# Bash &ndash; Bourne Again Shell

Un intérprete de comandos es el programa que se ejecuta cada vez que se comienza una sesión de tty o emulador de terminal.

* El programa por defecto en los sistemas Linux es **Bash**, denominado *shell* por proveer el entorno de trabajo.

* La shell provee **Environmental Variables**, las que contienen información sobre la máquina y sesión actuales.

* Un **prompt** detiene la ejecución de la shell, esperando la entrada de comandos por parte del usuario.

---

# Environmental Variables

Bash también es un lenguaje de programación que puede realizar operaciones tales como definir variables.

```
$ mascota="perro"
```

* Bash provee variables en mayusculas con información relativa a la máquina y sesión actual.

  * $USER - usuario de la sesión actual.
  * $SHELL - shell de la sesión actual.

---

# Imprimir variables

Bash ofrece los comandos *echo* y *printf* para imprimir en pantalla el contenido de las variables.

```
$ echo $SHELL
```

```
$ printf $SHELL
```

* La principal diferencia es que *printf* no imprime un salto de linea y el prompt se concatena al texto impreso en pantalla.

---

# Prompt

Texto que antecede a la entrada del usuario, generalmente con información sobre el entorno de trabajo actual.

```
user@machine directory $
```

* `user` - usuario de la sesión actual.
* `machine` - máquina que ejecuta el sistema operativo.
* `directory` - *working directory* de la shell.
* `$` - *user* no puede editar archivos fuera de $HOME.

---

# Working Directory

Ubicación de la shell dentro del árbol de directorios del sistema.

* $PWD -  directorio actual de la shell.
* $OLDPWD - el antiguo contenido de $PWD.

Ambas pueden imprimirse en pantalla con *echo* o *printf*.

