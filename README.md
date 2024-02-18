# arbol-geneal-gico
import networkx as nx
import matplotlib.pyplot as plt

 Crear un grafo dirigido para representar el árbol genealógico
G = nx.DiGraph()

 Agregar nodos (individuos)
G.add_nodes_from(["Abuelo", "Abuela", "Padre", "Madre", "Hijo", "Hija"])

 Agregar relaciones (aristas)
G.add_edges_from([("Abuelo", "Padre"), ("Abuela", "Padre"),
                  ("Abuelo", "Madre"), ("Abuela", "Madre"),
                  ("Padre", "Hijo"), ("Padre", "Hija"),
                  ("Madre", "Hijo"), ("Madre", "Hija")])

 Dibujar el árbol genealógico
pos = nx.spring_layout(G)
nx.draw(G, pos, with_labels=True, node_size=2000, node_color="skyblue", font_size=10, font_weight="bold", arrowsize=20)
plt.show()
