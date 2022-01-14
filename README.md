# ejercicio_1103.sh
Resolución del ejercicio "1.10.3 Plant–Pollinator Networks"

###### literal 1.

- primero nos ubicamos en la carpeta con los datos que nos solicita el ejercicio, en este caso: 

Dell@DellG7Andres MINGW64 ~

$ cd Documents/

Dell@DellG7Andres MINGW64 ~/Documents

$ cd practica\ bio/

Dell@DellG7Andres MINGW64 ~/Documents/practica bio

$ cd csb-master

Dell@DellG7Andres MINGW64 ~/Documents/practica bio/csb-master

$ cd unix/

Dell@DellG7Andres MINGW64 ~/Documents/practica bio/csb-master/unix

$ cd data

- posteriormente procedemos a resolver el ejercicio, para lo cual primero nos pide que tomemos uno de los archivos ".txt" archivos y determina el número de filas (polinizadores) y columnas (plantas), para lo cual primero utilizamos:

Dell@DellG7Andres MINGW64 ~/Documents/practica bio/csb-master/unix/data

$ cat Saavedra2013/n10.txt | wc -l

14

- luego contamos las columnas sin tomar en cuenta los espacios para lo cual usamos:

Dell@DellG7Andres MINGW64 ~/Documents/practica bio/csb-master/unix/data

$ head -n 1 Saavedra2013/n10.txt | tr -d ' ' | tr -d '\n' |wc -c

20

- Y esto seria todo en cuanto al primer literal


###### Literal 2.

- en este literal nos pide que imprimamos el numero de filas y columnas para cada red, para lo cual utilizaremos:

Dell@DellG7Andres MINGW64 ~/Documents/practica bio/CSB-master/unix/data

$ FILES=Saavedra2013/*.txt

- con esto le decimos a la maquina que cree una lista con todos los archivos ".txt" en una variable de nombre "FILAS", Luego replicar varias veces un proceso a través de todos los archivos en el directorio con un bucle "for" para lo cual utilizaremos la siguiente linea de comandos:

Dell@DellG7Andres MINGW64 ~/Documents/practica bio/CSB-master/unix/data

$ for f in $FILES

 do echo $f

 done

- esto nos imprimiría los nombres de archivo en el directorio:


Saavedra2013/n1.txt

Saavedra2013/n10.txt

Saavedra2013/n11.txt

Saavedra2013/n12.txt

Saavedra2013/n13.txt

Saavedra2013/n14.txt

Saavedra2013/n15.txt

Saavedra2013/n16.txt

Saavedra2013/n17.txt

Saavedra2013/n18.txt

Saavedra2013/n19.txt

Saavedra2013/n2.txt

Saavedra2013/n20.txt

Saavedra2013/n21.txt

Saavedra2013/n22.txt

Saavedra2013/n23.txt

Saavedra2013/n24.txt

Saavedra2013/n25.txt

Saavedra2013/n26.txt

Saavedra2013/n27.txt

Saavedra2013/n28.txt

Saavedra2013/n29.txt

Saavedra2013/n3.txt

Saavedra2013/n30.txt

Saavedra2013/n31.txt

Saavedra2013/n32.txt

Saavedra2013/n33.txt

Saavedra2013/n34.txt

Saavedra2013/n35.txt

Saavedra2013/n36.txt

Saavedra2013/n37.txt

Saavedra2013/n38.txt

Saavedra2013/n39.txt

Saavedra2013/n4.txt

Saavedra2013/n40.txt

Saavedra2013/n41.txt

Saavedra2013/n42.txt

Saavedra2013/n43.txt

Saavedra2013/n44.txt

Saavedra2013/n45.txt

Saavedra2013/n46.txt

Saavedra2013/n47.txt

Saavedra2013/n48.txt

Saavedra2013/n49.txt

Saavedra2013/n5.txt

Saavedra2013/n50.txt

Saavedra2013/n51.txt

Saavedra2013/n52.txt

Saavedra2013/n53.txt

Saavedra2013/n54.txt

Saavedra2013/n55.txt

Saavedra2013/n56.txt

Saavedra2013/n57.txt

Saavedra2013/n58.txt

Saavedra2013/n59.txt

Saavedra2013/n6.txt

Saavedra2013/n7.txt

Saavedra2013/n8.txt

Saavedra2013/n9.txt


- FInalmente  determinaremos todo con el siguiente comando:

Dell@DellG7Andres MINGW64 ~/Documents/practica bio/CSB-master/unix/data

$ for f in $FILES

 do myrow=`cat $f | wc -l`

 echo $f $myrow

 done

- Y ese seria todo nuestro literal 2



#### Literal 3
  
- En este literal nos pide averiguar ¿Cuál es la red con el mayor número de filas? ¿Cuál es el que tiene el mayor número de columnas? para lo cual utilizaremos el siguiente comando 


Dell@DellG7Andres MINGW64 ~/Documents/practica bio/CSB-master/unix/data

$ bash netsize_all.sh | sort -n -r -k 2 | head -n 1

../data/Saavedra2013/n58.txt 678 90

- y de manera simila:

Dell@DellG7Andres MINGW64 ~/Documents/practica bio/CSB-master/unix/data

$ bash netsize_all.sh | sort -n -r -k 3 | head -n 1

../data/Saavedra2013/n56.txt 110 207


### FIN DEL EJERCICIO
