---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
footer: Material OSEC - CC BY-NC-SA
---

# **Máquina**

Introducción a las *máquinas computadoras*.
Introducción a la *CPU* y *almacenamiento*.
Introducción al *Sistema Operativo*. 

---

# ¿Qué es una computadora?

Una computadora es una máquina electrónica capaz de:

* Realizar una representación digital de la información.
  * Trabaja letras y números como datos en 0's y 1's.
* Procesar la información de entrada.
  * Ejecuta operaciones lógicas y aritméticas.
* Realizar una salida de información.
  * Retorna en papel u otro medio.

---

# ¿Qué componentes la conforman?

* Unidad de almacenamiento.
  * Componente que contiene datos en binario.
* Entrada de información.
  * Medio por el que recibe los datos a procesar.
* Unidad de procesamiento.
  * Componente que lee y opera en la entrada.
* Salida de información.
  * Medio por el que retorna los datos procesados.

---

# Punched card

Las tarjetas perforadas son la forma de interacción más antigua con las máquinas computadoras.

* Una tarjeta perforada representa datos en forma binaria.
* La máquina recibe la tarjeta perforada como entrada.
* La máquina opera conforme sus instrucciones programadas.
* La máquina emite su salida perforando una nueva tarjeta.

---

# Automaton

Las máquina de tarjetas perforadas se comportan como un autómata, esto es, ejecutan un conjunto de instrucciones predeterminadas.

* La máquina no retiene información.
* Las operaciones deben programarse en la máquina.
* Convertir información a una tarjeta requiere trabajo adicional.
* Se trabaja en lenguaje binario, ilegible para las personas.

---

# Storage unit

La primera gran mejora a las máquinas computadoras ocurrió con la aparición de las unidades de almacenamiento.

* La máquina ahora es capaz de retener información.
* Puede almacenarse más información en menos volumen.
  * Primero cintas magnéticas (e.g. floppy, cassettes, VHS's).
  * Luego discos rotatorios (HDD).
  * En el presente unidades de estado sólido (SSD, M.2).

---

# CPU &ndash; Central processing unit

La segunda gran mejora a las máquinas computadoras ocurrió con la aparición de las unidades centrales de procesamiento.

* La máquina ahora puede re-programarse.
* Se introducen los lenguajes de programación de bajo nivel.
  * *Assembly*, lenguaje de máquina.
* Se introducen los lenguajes de programación de alto nivel.
  * *C*, compilado a lenguaje de máquina.

---

# Resource management

La introducción de las cintas magnéticas y las CPU's traen consigo una mayor capacidad de computación.

Los lenguajes de programación construyen programas complejos que se ejecutan de forma autónoma dentro de la máquina.

La administración de recursos ya no puede realizarse de forma manual, se vuelve necesario que la máquina se administre a sí misma.

---

# Operating System

* El sistema operativo se encarga de administrar la máquina.

  * Es un programa que se ejecuta en prioridad máxima.

* Los programas deben pedir los recursos al sistema operativo.

  * Las *llamadas al sistema* permiten acceso al almacenamiento.

* La interacción humana con la máquina es un programa más.
  * El *intérprete de comandos* permite interactuar con el S.O.

* El concepto de máquina se abstrae bajo la palabra *computadora*.