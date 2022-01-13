# ejercicio_1103.sh
Resolución del ejercicio "1.10.3 Plant–Pollinator Networks"
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

- posteriormente procedemos a resolver el ejercicio, para lo cual primero nos pide ue tomemos uno de los archivos ".txt" archivos y determina el número de filas (polinizadores) y columnas, para lo cual primero utilizamos:

Dell@DellG7Andres MINGW64 ~/Documents/practica bio/csb-master/unix/data
$ cat Saavedra2013/n10.txt | wc -l
14

- luego contamos las columnas sin tomar en cuenta los espacios para lo cual usamos:

Dell@DellG7Andres MINGW64 ~/Documents/practica bio/csb-master/unix/data
$ head -n 1 Saavedra2013/n10.txt | tr -d ' ' | tr -d '\n' |wc -c
20

- Y esto seria todo en cuanto al primer literal
