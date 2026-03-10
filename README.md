**Recorridos en Grafos con BFS y DFS en Python**

Este proyecto implementa dos algoritmos fundamentales de recorrido en grafos:

BFS (Breadth First Search) – Búsqueda en anchura

DFS (Depth First Search) – Búsqueda en profundidad

Los algoritmos se aplican sobre un árbol representado como un diccionario en Python.


**Estructura del árbol**

El árbol se representa utilizando un diccionario donde:

la clave es el nodo

el valor es una lista de sus hijos

tree = {
    'A': ['B', 'C'],  
    'B': ['D', 'E'],  
    'C': ['F', 'G'],  
    'D': ['H', 'I'],  
    'E': ['J', 'K'],  
    'F': ['L', 'M'],  
    'G': ['N', 'O'],  
    'H': [], 'I': [], 'J': [], 'K': [],  
    'L': [], 'M': [], 'N': [], 'O': []
}

**BFS – Breadth First Search**

El algoritmo BFS recorre el árbol por niveles, utilizando una cola (queue).

Primero visita el nodo inicial, luego todos sus vecinos, después los vecinos de esos nodos, y así sucesivamente.


**DFS – Depth First Search**

El algoritmo DFS recorre el árbol profundizando primero en cada rama antes de regresar.

Se implementa normalmente usando recursividad
    
