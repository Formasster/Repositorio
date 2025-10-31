# Ejercicio Linux - capitulo 2

****



[TOC]



## Comandos utilizados 

``pwd`` - directorio actual 

``ls`` - lista desde el directorio actual    ``-a`` (tb archivos ocultos) ``-l``(detalles) ``-h``(tamaño)

``man`` - manual

``cat`` - muestra por pantalla el contenido y, cuando termina, vuelve a la línea de comandos. 

``more`` - muestra contenido

``less`` - permite moverse por el contenido

``head y tail`` - mostrar por el nombre y por el final del archivo (si ``-nx`` puedes cambiar nº de líneas )

``touch`` - crear archivo 

``ee`` - edición rápida  ``vi`` - editor linux

``mcedit`` [archivo] - abrir el editor  

`` -lSh`` - listado largo ordenado por tamaño y con tamaños legibles 

![image-20250924111107366](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250924111107366.png)

## Estructura de carpetas Linux

![image-20250924102016703](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250924102016703.png)

## Ejercicios

1. ¿En qué directorio se encuentran los ficheros de configuración del sistema?

Está ubicado en la carpeta /etc

3. Muestra el contenido del directorio actual. 

```bash
$ ls
```

![image-20250924111610589](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250924111610589.png)

4. Muestra el contenido del directorio que está justo a un nivel superior. 

   ```bash
   $ cd ..
   $ ls
   ```

   ![image-20250926104300378](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926104300378.png)

5. ¿En qué día de la semana naciste?, utiliza la instrucción cal para averiguarlo. 

Miramos por el marzo del 2006

```bash
$ cal 3 2006
```

![image-20250926104937880](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926104937880.png)

6. Muestra los archivos del directorio /bin 

```bash
$ cd bin
//tenemos en cuenta que estamos en el directorio raíz
$ lsls
```

![image-20250926105400257](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926105400257.png)

La lista es demasiado larga, así que no hemos capturado todo. 

7. Suponiendo que te encuentras en tu directorio personal (/home/nombre), muestra un listado del contenido de /usr/bin a) con una sola línea de comando, b) moviéndote paso a paso por los directorios y c) con dos líneas de comandos. 

```bash
//a
$ ls /usr/bin
```

```bash
//b
$ cd /usr
$ cd /bin
$ ls
```

```bash
//c
$ cd /usr/bin
$ ls
```

![image-20250926111027169](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926111027169.png)

8. Muestra todos los archivos que hay en /etc y todos los que hay dentro de cada subdirectorio, de forma recursiva (con un solo comando). 

```bash
$ tree
```

![image-20250926111334545](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926111334545.png)

9. Muestra todos los archivos del directorio /usr/X11R6/bin ordenados por tamaño (de mayor a menor). Sólo debe aparecer el nombre de cada fichero, sin ninguna otra información adicional. 

Esta carpeta mencionada (X11R6) no existe, así que no nos será posible acceder al directorio siguiente. 

10. Muestra todos los archivos del directorio /etc ordenados por tamaño (de mayor a menor) junto con el resto de características, es decir, permisos, tamaño, fechas de la última modificación, etc. El tamaño de cada fichero debe aparecer en un formato “legible”, o sea, expresado en Kb, Mb, etc. 

```bash
$ ls -lSh 
```

![image-20250926120425461](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926120425461.png)

11. Muestra todos los archivos del directorio /bin ordenados por tamaño (de menor a mayor). Sólo debe aparecer el tamaño y el nombre de cada fichero, sin ninguna otra información adicional. El tamaño de cada fichero debe aparecer en un formato “legible”, o sea, expresado en Kb, Mb, etc

```bash
$ cd /bin
$ ls -lShr 
```

![image-20250926120801875](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926120801875.png)

12. Muestra el contenido del directorio raíz utilizando como argumento de ls una ruta absoluta.

```bash
$ ls /
```

![image-20250926121015352](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926121015352.png)

13. Muestra el contenido del directorio raíz utilizando como argumento de ls una ruta relativa. Suponemos que el directorio actual es /home/elena/documentos. 

```bash
$ ls ../../.. 
```

![image-20250926121456695](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926121456695.png)

14. Crea el directorio gastos dentro del directorio personal. 

```bash
$ mkdir gastos
```

no sucede nada, pero podemos comprobar que se creó:  

![image-20250926121714224](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926121714224.png)

14. ¿Qué sucede si se intenta crear un directorio dentro de /etc? 

NO permite por falta de permisos.

15. Muestra el contenido del fichero /etc/fstab . 

```bash
$ cat /etc/fstab
```

![image-20250926122050447](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926122050447.png)

16. Muestra las 10 primeras líneas del fichero /etc/bash.bashrc 

```bash
$ head /etc/bashrc
```

![image-20250926122313704](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926122313704.png)

17. Crea la siguiente estructura de directorios dentro del directorio de trabajo personal: multimedia | -------------------------------------------------- | | | | musica imagenes video presentaciones | -------------- | | personales otras 

Mediante comando ``mkdir`` y la interfaz creamos lo siguiente: 

![image-20250926123044307](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926123044307.png)

18. Crea un fichero vacío dentro del directorio musica, con nombre estilos_favoritos.txt 

```bash
$ cd Música
$ tauch estilos_favoritos.txt
```



19. Utiliza tu editor preferido para abrir el fichero estilos_favoritos.txt e introduce los estilos de música que más te gusten. Guarda los cambios y sal. 

```bash
$ nano estilos_favoritos.txt
```

![image-20250926123819001](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926123819001.png)

20. Muestra todo el contenido de estilos_favoritos.txt 

```bash
$ cat estilos_favoritos,txt
```

![image-20250926124002686](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926124002686.png)

21. Muestra las 3 primeras líneas de estilos_favoritos.txt 

```bash
$ head -n3 estilos_favoritos.txt
```

![image-20250926124105403](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926124105403.png)

22. Muestra la última línea de estilos_favoritos.txt 

```bash
$ tail -n1 estilos_favoritos.txt
```

![image-20250926124205497](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926124205497.png)

No aparee nada porque la última línea está vacía

23. Muestra todo el contenido del fichero estilos_favoritos.txt excepto la primera línea. Se supone que no sabemos de antemano el número de líneas del fichero.

```bash
$ tail -n +2 estilos_favoritos.txt
```

![image-20250926124453850](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20250926124453850.png)

Líneas a partir de la sgunda 