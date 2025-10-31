# Ejercicios Linux - capitulo 3

****

[TOC]

<div style="page-break-after: always;"> </div>

****

## Comandos utilizados 

`-R` - recursivo 

![image-20251001104204638](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20251001104204638.png)

![image-20251001104235140](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20251001104235140.png)

## Ejercicios

1. Muestra todos los archivos del directorio actual que son imágenes jpg.

```bash
$ ls *.jpg
```

![image-20251001104754849](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20251001104754849.png)

No tenemos archivos con esta extensión, así que  no se muestra nada.

2. Muestra todos los archivos del directorio /usr/bin que empiecen por la letra j. 

```bash
$ ls /usr/bin/j*
```

![image-20251001110420612](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20251001110420612.png)

3. Muestra los archivos que empiecen por k y tengan una a en la tercera posición, dentro del directorio /usr/bin. 

```bash
$ ls /usr/bin/k?a*
```

![image-20251001105956482](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20251001105956482.png)

4. Muestra los archivos del directorio /bin que terminen en n. 

```bash
$ ls /bin/*n
```

![image-20251001110252946](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20251001110252946.png)

5. Muestra todos los archivos que hay en /etc y todos los que hay dentro de cada subdirectorio, de forma recursiva. 

```bash
$ ls -R /etc
//o
$ tree /etc
```

![image-20251001110915545](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20251001110915545.png)

6. Crea un directorio en tu directorio de trabajo con nombre prueba. Copia el archivo gzip del directorio /bin al directorio prueba. Crea un duplicado de gzip con nombre gzip2 dentro de prueba. 

```bash
$ mkdrir prueba 
$ cp /bin/gzip2 prueba 
```

![image-20251001111332456](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20251001111332456.png)

2. Cambia el nombre de prueba a prueba2. Crea prueba3 en el mismo nivel que prueba2 y mueve todos los ficheros de prueba2 a prueba3. Borra prueba2. 

```bash

```



2. Crea un fichero vacío con nombre “*?Hola caracola?*”. ¿Se puede? En caso de que se pudiera, ¿sería recomendable poner nombres así? Razona la respuesta.

```bash

```