#shu chuan chu, jhon roddick, Chen-Jen Su, ...
#DensityClusteringChuACO2004.pdf
#Resumen 

## Algoritmo Constrained ACO

añade restricciones a momento de calcular la fuerza de la feromona, con las siguientes propiedades:

* aplica la metrica cuadratica combinada con la suma K distancias de vecinos mas cercanos, en lugar de la distancia euclideana
* La feromona es actualizada en funcion de un unbral de distancia estadistico
* reduce el rango de busqueda

## Algoritmo
ACODF usa simulated anneling, algoritmos geneticos, y cada hormiga solo visita una fraccion del total de objetos (clusters)
y el numero de objetos visitados decrementa en cada ciclo.
ACODF no maneja clusters con formas arbitrarias, con outliers o con enlaces puentes. 

Dado un objeto en la posicion O y objetos Xi, i=1,2,3...T 
T es el numero total de objetos.

### estrategia 1
Dq(O,Xm) = (O-Xm) exp t W exp -1 (O-Wm)

(O-Xm) es un vector columna de error
W matriz de covarianza

W = 1/T * sumatoria i=1 to T (Xi - Xmedia) (Xi -Xmedia) exp t

i y m son los mismos valores?? en el calculo de la covarianza??
 t minuscula quien es?

### estrategia 2
usan SKNND, distancia de los vecinos mas cercanos para identificar cluster basados en desidad.
al usar SKNND la probabilidad de moverse a un cluster mas denso aumenta. esta estrategia evita errores
cuando existen enlaces puentes entre clusters.


### estrategia 3
La actualizacion de la feromorna es inversamente proporcional a la distancia de los objetos visitados
si el objeto se encuentra muy lejos la fuerza de la ferormona se actualiza debilmente, y viceversa.
para compensar esto un limite estadistico para k hormiga es adoptado:

* Lts k =  AVG L path k + StDev L path k
    * AVG Lpathk : distancia promedio
	AVG Lpath = Sumatoria de  Lij / E
	E = numero de paths visitados por la hormiga k
	Lij = distancia entre i y j
	si Lijk > Lts k, Xi y Xj se encuentran en diferentes clusters, en funcion de esto la distancia de Xi y Xj 
	no puede ser añadida en el tamaño del path y la feromorna no puede ser actualizada entre esos objetos.
    * StDev Lpathk : desviacion estandar para la ruta de los objetos visitados por la hormiga k

* una hormiga por cada objeto o cluster? la inicializacion setea uno a uno, tambien la feromorna con un valor positivo.

* feromorna es como la jalea del HBMO??


### conclusiones

Parametros importantes en el resultado de clustering
N1 numero de objetos a ser visitados en cada ciclo por cada hormiga, 
si N1 es muy pequeño las hormigas no pueden visitar todos los puntos que pertenecen al mismo cluster, resultando 
gran cantidad de subclusters delgados. 

Y influyen cuando el cluster tiene outliers y enlaces puentes entre otros clusters, cantidad de hormigas??a 40
Y = [5-15] 

* parametro del dbscan:
    * Following the recommendation of Ester et al., M inP ts was fixed to 4 and  was changed during the experiments

### me
 compararon DBSCAN, vs CURE vs CACO.
 CACO WIN.


