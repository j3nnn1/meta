
#Resumen 
* Stephan Scheuerer
* Rolf Wendolsky

#Capacited Cluster Problem

Establece un limite de individuos por cada cluster.
CCP esta relacionado con el problema p-median (p-mediana??)
CCP es un problema "NP-Complete" si los centros del cluster NO son definidos.

aca se define un modelo de programacion lineal para este problema.

# Revision de literatura
CCP fue introducido por **MULVEY AND BECK**  y ha sido estudiado extensivamente en clustering y teoria de localizacion?? location theory

* **Koskosidis and Powell**
* **Maniezzo **
*  y en un contexto relacionado por *Fisher y Jaikumar*.

    #Otros autores proponen un enfoque de DOS pasos
    - Consiste en una seleccion de centros y una fase de asignacion.
    - *Pirkul* describe una rama y un procedimiento limite que usa la aproximacion langragiana 
    - El enfoque anterior y una busqueda local fue propuesto por Lorena y Senna
    - Baldaci propone usar un algoritmo basado en particionamiento
    - Osman y Christofides desarrollan un algoritmo basado en Simulated Anneling/Tabu Search para resolver este problema.
    - Manniezo aplico un algoritmo binomico.
    - Ahmadi, desarrollo un enfoque basado en densidad y un procedimiento eficiente de busqueda local para mejora.
    - Actualmente es uno de los mejores metodos para CCP, es un adaptativa heuristica basada en tabu search desarrollado por Franca.

El paper trata de clustering aplicado a CPP, y utiliza c++ como lenguaje de implementacion.

