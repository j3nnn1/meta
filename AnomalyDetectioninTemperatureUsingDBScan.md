# Resumen de  Mete Celik, Filiz DADASER-Celik, ahmet sakir dokuz
**DBScan** es un algoritmo de cluster basado en densidad.
Descubrimiento de patrones en series de tiempo, *deteccion de anomalias en series de tiempo*

* Las tècnicas de detecciòn de anomalias puede ser clasficadas en: 
    - Enfoque estadistico, crea un modelo estadistico de la data e identifica que data no se ajusta al modelo
    - Enfoque basado en distancia, "the data at a distance greater than a pre-defined distance is called an anomaly"

## Algoritmo DBSCAN
* requiere dos parametros definidos por el usuario
    * neighborhood distance epsilon (eps)
    * minimo numero de puntos (minpts)
* si el numero de puntos vecinos de un punto es mayor que minpts este grupo es llamado cluster/conglomerado/grupo
* DBSCAN etiqueta los puntos como:  puntos nucleo, puntos bordes, puntos anomalos (outliers)
    * puntos nucleo: son aquellos que tienen al menos minpts numero de puntos separados con la distancia eps.
    * puntos borde: son vecinos de los puntos nucleo, y no cumplen las condiciones para ser puntos nucleo.
    * puntos outliers: son definidos como outliers o anomalos si no cumplen los anteriores, y ademas no tiene el minpts de puntos para ser un cluster.

## Algoritmo
m = total de filas del dataset
D = dataset
class_no = 1

For i=1 to m
    Dist = distance(i, D) // todas las distancias hacia ese punto (matriz) // elijo centro de gravedad, punto centrico
    // y the distances between center point D[i] and remaining points i
    neighbors = find(Dist <= Eps) // obtengo solo los puntos que cumplen la condicion de epsilon (matriz) 4 the points whose distances are less than or equal to eps, are accepted as neighbors of the center point D[i]
    neighbors_count = count(neighbors) // cuento cantidad de puntos // escalar
    coreNeig = check_core_neighbors(neighbors) // obtengo matriz que contiene los puntos que son core, matriz true | false
    if neighbors_count >= minpts
    	class(i) = class_no // creo un nuevo cluster
        while more points near i
	    class(point) = class_no
	end while
	class_no += 1
    else if (neighbors_count < minpts & coreNeig= True)
        class(i) = 0 // border point
    else if (neighbors_count < minpts)
        class(i) = -1 //outlier
end For
return class // vector con el numero de cluster o pertenencia de un registro

