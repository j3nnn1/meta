#Capitulo 9 clustering, Resumen

*Define Clustering/segmentacion/conglomerados/componentes como un metodo descriptivo, con dos propriedades: el numero de clusters no es definido con anterioridad y son combinaciones de objetos que tienen caracteristicas similares.
*Otra definicion: Reconocimiento de patrones no supervisado.
*Crean subconjuntos con poblaciones homogeneas (kmeans)
*Sirve para: identificar valores extremos.
*La distancia puede variar en funcion de los datos. (euclidean, manhattan)
*En algunos analisis de clutering la distancia euclideana es sustituida por el coeficiente de pearson r.

##Listado de los metodos de particionamiento:

- moving centres, kmeans, dynamic clouds
- kmedoides, kmodes, kproptotypes
- kohonen networks
- clustering by similarity aggregation

**principios de analisis relacional**, se basa en representar la data en forma de relaciones equivalentes. un cluster o conglomerado es una relacion en R donde i R j si i y j estan en el mismo cluster como por cualquiera relacion binaria definida para un conjunto de objetos podemos asociar R con una matriz nxn


## Division por el tipo de metodo, ambos usan el concepto de distancia o densidad:

* agglomerative, metodo jerarquico ascendente. se separa en single linkage or complete methods

* divisive, metodo jerarquico descendente

* Clustering de agregacion por similaridad permite al algoritmo determinar el numero optimo de clusters automaticamente.

* Un buen cluster puede detectar la estructura presente en la data, habilitar el numero optimo de clusters.

## Orden de complejidad: (cuando k esta definido)

* **kmeans:** If k and d (the dimension) are fixed, the problem can be exactly solved in time where n is the number of entities to be clustered

	O(n exp dk+1 log(n)) *Forgy*

	O(nkdi) *LLoyds*  where n is the number of d-dimensional vectors, k the number of clusters and i the number of iterations needed until convergence

* **pam:**

	O(n exp 2)

	Buscar esta referencia?

	* Forgy EW. 1965 Cluster Analysis of multivariate data: efficiency versus interpretability of classification.

## Desventajas de los metodos de particionamiento:

- el final particionamiento depende de en su mayoria de la seleccion de los centros de gravedad/ centroides / ci por lo cual no siempre se optiene un optimo global.

- kmeans, solo detecta buenos grupos con la forma esferica.

- los algoritmos con single linkage son menos adecuados para detectar clusters esfericos, sin embargo tiene buenas propiedades teoricas y son efectivos para detectar elengados, irregulares y sinuosos clusters.

- Metodo de agregacion por similitud es afectado por la presencia de variables redundantes, las cuales sesgan el resultado en favor de estas variables, ya que comienzan a ser ser discrimitativas.
		  
## Libro
* Stephane Tuffery

