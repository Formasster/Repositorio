# Permisos Linux

****

[TOC]



<div style="page-break-after: always;"> </div>

## Ejercicio - 1

Crea un archivo prueba.txt y dale permisos rw-r----- usando modo simbólico

```bash
$ touch prueba.txt
$ chmod u=rw,g=r,o= prueba.txt
```

![image-20251001100355601](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20251001100355601.png)

También comprobamos que los permisos se han dado

## Ejercicio - 2

Haz que solo el grupo pueda escribir en notas.txt .

```bash
$ touch notas.txt
$ chmod g+w,u-w,o-w notas.txt
```

![image-20251001100721385](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20251001100721385.png)

## Ejercicio - 3  

Cambia el propietario de tarea.doc a ana y el grupo a profes.

```bash
$ sudo adduser ana
$ sudo groupadd profes
$ sudo chown ana:profes prueba.txt
```

![image-20251001102221012](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20251001102221012.png)

Primero creamos el usuario y el grupo

![image-20251001102246250](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20251001102246250.png)

![image-20251001102313401](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20251001102313401.png)

## Ejercicio - 4 

Quita todos los permisos a “otros” sobre config.cfg .

```bash
$ touch config.cfx
$ chmod o-rwx config.cfx
```

![image-20251001102638283](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20251001102638283.png)

## Ejercicio - 5 

Pon rwx a todos en un script llamado run.sh.

```bash
$ touch run.sh
$ chmod a+rwx run.sh
```

![image-20251001102842743](C:\Users\2dawd24\AppData\Roaming\Typora\typora-user-images\image-20251001102842743.png)