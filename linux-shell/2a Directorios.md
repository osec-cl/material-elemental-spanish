---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
footer: Material OSEC - CC BY-NC-SA
---

# **Visualizando $HOME**

Introducción al coreutil *ls*.
Introducción al builtin *pwd*.
Convensiones de directorios y *dotfiles*.

---

# ¿Dónde estoy?

La shell de Linux siempre se ubica en un directorio.

```
$ pwd
```

* Puede leerse como *Print Working Directory*.

* Por defecto es `/home/user` para el *user* de la sesión.

  * A este directorio se le conoce como $HOME


---

# ¿Qué hay aquí?

Cada directorio contiene a un conjunto de archivos.

```
$ ls
```

* Puede leerse como *List*.

* Imprime los archivos y directorios en el *Working Directory*.

---

# ¿Hay más aquí?

Algunos archivos fueron suprimidos, para incluirlos:

```
$ ls -a
```

* Puede leerse como *List all*

* No ignora los archivos que empiezan con un punto.