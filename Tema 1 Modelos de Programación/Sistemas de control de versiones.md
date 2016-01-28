
#Sistemas de Control de Versiones (VCS)

Un sistema de control de versiones es una herramienta de programación que registra cambios en ficheros a lo largo del tiempo. Pueden ser:

-	**Locales:** Información en una única máquina. Almacena las versiones en distintos directorios. Ejemplo: rcs.

![Sistemas de Control de Versiones Locales](https://git.lumc.nl/l.khachatryan/programming-course/raw/d97c99773ddcb3d560cb88394791700abf4666f1/images/local_vcs.png)

-	**Centralizados:** Son una evolución de los sistemas locales para conseguir trabajar en varias máquinas y poder colaborar.Servidor central de ficheros al que hay que conectarse para poder trabajar y que trabaja con diferencias con respecto a otras máquinas. Surgen problemas con los conflictos en los cambios.
![Sistemas de Control de Versiones Centralizados](https://git-scm.com/figures/18333fig0102-tn.png)

-	**Distribuidos:** A parte del servidor central del ficheros tenemos una copia de la base de datos en cada máquina y por lo tanto no es necesario conectarse al servidor central de ficheros para trabajar dependiendo de las tareas que vayamos a realizar. Son más flexibles. Ejemplos: Git, Mercurial.

![Sistemas de Control de Versiones Distribuidos](https://git-scm.com/figures/18333fig0103-tn.png)


----------

##![GIT](https://git-scm.com/images/logo@2x.png) 
[PRO-GIT](https://git-scm.com/book/es/v1)

Git es un sistema de control de versiones distribuido que se caracteriza por:

1.  Trabaja con instantáneas y no con diferencias.
2.  Tiene integridad.
3.  Casi cualquier operación se puede llevar a cabo de forma local.
4.  No se pierde información, ya que con cualquier nueva versión solo añade información y no borra con respecto a versiones anteriores.

###¿Qué es un repositorio?
Lugar en el que se almacenan los datos actualizados e históricos de una implementación además de ciertos metadatos.

