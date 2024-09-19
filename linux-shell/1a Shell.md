---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
footer: Material OSEC - CC BY-NC-SA
---

# **Intérprete de Comandos**

Introducción a los *macro processors*.
Reconocer elementos en una *shell*.

---

# Unix Shell

Una shell de UNIX es un **macro procesador**.

* Un intérprete de comandos se limita a ejecutar línea a línea los comandos que le son entregados en la entrada.

* Un macro procesador puede *expandir* texto y símbolos de la entrada para crear expresiones de mayor envergadura.

* Una shell de UNIX es un intérprete de comandos y un lenguaje de programación, lo que permite automatizar tareas.

---

# Shell Session

Una sesión de shell es un puente entre la persona frente a la computadora y el sistema operativo.

* **TTY** &ndash; Establece el tipo de sesión más directa con la computadora, es entregada por el sistema operativo y todo sistema UNIX la tiene.

* **PTY** &ndash; Es una sesión hija de una TTY y vuelve posible que los sistemas UNIX provean una sesión por usuario.

* **PTS** &ndash; Es una sesión hija de una PTY, permite que un usuario pueda abrir múltiples emuladores de terminal al mismo tiempo.

---

# (Non) Login + (Non) Interactive

* **Inicio de sesión + Interactiva**
  * Ocurre al abrir una TTY o PTY.

* **No inicio de sesión + Interactiva**
  * Ocurre al abrir una PTS.

* **Inicio de sesión + No interactiva**
  * Ocurre al enviar comando remoto.

* **No inicio de sesión + No interactiva**
  * Ocurre al ejecutar un *script*.

---

# Script

Un *script* es un listado secuencial de comandos a ejecutar.

* Su objetivo es automatizar tareas que de otra forma deberían ser ejecutadas manualmente.

* El intérprete de comandos es capaz de utilizar los programas en PATH para llevar a cabo las tareas.

* El lenguaje de programación provisto por el macro procesador permite otorgar lógica como condiciones o bucles.

---

# Bash &ndash; Bourne Again Shell

El programa *Bash* es el macro procesador por omisión en los sistemas Linux, compatible con todos los sistemas basados en UNIX.

* Se ejecuta cada vez que una persona (real) o un usuario (virtual) ejecuta una sesión de TTY o PTY/PTS, respectivamente.

* Esta shell provee **Environmental Variables**, las que contienen información sobre la computadora y sesión actuales.

* Un **prompt** detiene la ejecución de la shell, esperando la entrada de comandos por parte del usuario.

---

# Environmental Variables

El lenguaje de programación permite definir variables.

```
$ mascota="perro"
```

* Las variables de entorno son las provistas por la shell.

  * **\$USER** &ndash; usuario de la sesión actual.
  * **\$SHELL** &ndash; shell de la sesión actual.
  * **\$PATH** &ndash; conjunto de directorios con ejecutables.


---

# Imprimir variables

Bash ofrece los comandos *echo* y *printf* para imprimir en pantalla el contenido de las variables.

```
$ echo $mascota
```

```
$ printf $mascota
```

* La principal diferencia es que *printf* no imprime un salto de linea y el prompt se concatena al texto impreso en pantalla.

---

# Prompt

Texto que antecede a la entrada del usuario, generalmente con información sobre el entorno de trabajo actual.

```
user@computer directory $
```

* `user` - usuario de la sesión actual.
* `computer` - computadora que ejecuta el sistema operativo.
* `directory` - directorio de trabajo actual de la shell.
* `$` - *user* no puede editar archivos fuera de $HOME.

---

# Working Directory

Ubicación de la shell dentro del árbol de directorios del sistema.

* **\$PWD** &ndash;  directorio actual de la shell.
* **\$OLDPWD** &ndash; el antiguo contenido de *\$PWD*.

Ambas pueden imprimirse en pantalla con *echo* o *printf*.

* **\$HOME** &ndash; por omisión cada nueva sesión de shell establecerá el directorio de trabajo al valor de esta variable.

