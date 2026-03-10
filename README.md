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

from collections import deque

def bfs(grafo, nodo, visitados=None):
    if visitados is None:
        visitados = set()

    cola = deque([nodo])
    visitados.add(nodo)

    while cola:
        actual = cola.popleft()
        print(actual)

        for vecino in grafo[actual]:
            if vecino not in visitados:
                visitados.add(vecino)
                cola.append(vecino)
        A
      /   \
     B     C
    / \   / \
   D   E F   G
  / \ / \ / \ / \
 H  I J K L M N O
