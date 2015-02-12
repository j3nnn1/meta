# Resumen de "Spatio-Temporal Outlier Detection in Large Database"
Derya Birant, Alp Kut

# un enfoque de tres pasos para eliminar outliers

* clustering
* checking spatial neighbors
* checking temporal neighbors

# DBScan para buscar outliers
# Enfoque de deteccion de outliers
* basados en la distribucion, usa una distribucion estandar estadistica. Ellos aplican un modelo de distribucion y reconocen los outliers que no se ajusten al modelo.
    multiples test deben realizarse para concer a que distribucion se ajusta la data, y aun asi puede no producir resultados satisfactorios.
* basados en clustering, no estan optimizados para detectar outliers.
* basados en la profundidad (depth-based), esta basado en geometria computacional, y calcula diferentes capas de k cascos convexos. Inficientes para dataset muy grandes.

* basados en la distancia, usa una metrica de distancia, para medir la distancia entre los puntos.
* basados en la densidad, dbscan . 

