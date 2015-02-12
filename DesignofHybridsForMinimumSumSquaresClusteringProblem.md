
#Joaquin Pacheco
#Design  of Hybrids of the minimum sum of square clustering problem
metaheuristicas propuestas para mejorar la calidad de reconocimiento de patrones. Especialmente con pequenios numeros de clusters.

*Algoritmos estudiados:* Tabu search, Local Search, Operadores geneticos.


Problema de minima suma de cuadrados en clustering.
===================================================

Es encontrar una particion de X (X es un conjunto de puntos) en m subconjuntos disjuntos entonces la suma de la distancia al cuadrado por cada punto al centroide
de su cluster es minima.

Analisis de cluster es un analisis exploratorio, usado para el reconocimiento de patrones.
Esto corresponde al area de clusters no jerarquicos.

Literarura previa:
==================

para dataset de 0 a 150.
* Koontz 1975
* Diehr 1985
* Merle 2000
para datasets > 150 , es necesario el uso de heuristicas.

Las mas populares son las basadas en metodos de busqueda local.
Kmeans  (Jancey 1966) es metodo de busqueda local.
Hmeans (Howard 1966)
Hansen y Mladenovic (2001) proponen Jmeans, y Hmeans+, HK-means.
Klein and Dubes con Simulated Anneling (1989)
Al-Sultan con Tabu Search 1995.
Babu and Murty, Algoritmos geneticos 1993.
Variable Neirghborhood search VNS Merle 2000
Hansen y Mladenovic en 2001.
Jhon Holland 1975, Adaptacion en sistemas naturales y artificiales

*Algoritmo memetico* la union entre un algoritmo genetico y un algoritmo de busqueda local? o son algoritmos hibridos?

Tabu search
===========

1989-1990 Glover, 


Explora el espacio de soluciones.
una vez que el optimo local es alcanzado.
se mueve hacia adelante o hacia aquellos que empeoran la solucion.
El ultimo movimiento es marcado como tabu durante las siguientes iteraciones para evitar ciclos.

Algoritmo Tabu search + Kmeans
=============================
Una vez que el punto X se mueve del Cluster C1 al cluster C2, es asignado a una lista tabu,
donde se evita que el punto X sea asignado nuevamente al Cluster C1 por un cierto numero de 
iteraciones definido.

Matrix_tabu = el numero de iteraciones en el cual el punto x deja el cluster C1

P = solucion inicial. P = particion/partition

Tabu_Tenure = indica el numero de iteraciones, donde un punto X no tiene permitido retornar to leaving the cluster

max_ite indica el numero maximo de iteraciones, unimproved ? desmejora? o sin mejora?

despues de diferentes pruebas Tabu_ternure = m

Algoritmo Tabu search + binary tree
===================================

HP(k) => indica el movimiento (i, j) localizado en el nodo k del arbol.
Q(i, j) = almacena el arbol binario que NO contiene los movimientos tabues.
si Q(i, j) = 0 es un movimiento tabu.
si es distinto de 0, es la cantidad de veces que el punto X se ha movido de i a j

numero de nodos en el arbol binario es = N (m-1)
N points. (numero de individuos/filas)
m es un entero positivo. m disjoint subsets. m = numero de clusters/conglomerados/grupos

Con respecto al metodo anterior, el resultado es el mismo pero el tiempo de calculo es menor con arboles binarios.

Algoritmo tabu search + algoritmo genetico.
===========================================

* jhon Holland 1975
* Revisar Algoritmo genetico.
* Las soluciones estan representadas por un conjunto de m puntos semillas.
* P = C1, C2, C3.. Cm es el resultado de asignar cada punto de X a cada semilla cercana.
* ‘non-goodness' dado por la funcion objetivo f de cada particion.
* La probabilididad de seleccion de una solucion esta dado por fmax - fi, fmax maximo valor de fi de esa poblacion

Memetic Algoritmos <> Algoritmos geneticos <> Algoritmo hibrido
================================================================

"local search procedures with crossing or mutating
operators; due to their structure some researchers have called them Hybrid Genetic
Algorithms, Parallel Genetic Algorithms (PGAs) or Genetic Local Search methods"

notas
=====
Interesante graficos y como realiza las comparaciones entre los diferentes algoritmos.
usa 10 ejecuciones con los mismos parametros por cada algoritmo, muy parecido a redes neuronales.
y grafica la desviacion con respecto a la mejor solucion.


