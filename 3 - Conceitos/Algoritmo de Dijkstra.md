# Algoritmo de Dijkstra
---
## Área de Estudo: Grafos e Algoritmos
---
## Explicação

O algoritmo de Dijkstra resolve o problema do **caminho mínimo** em
grafos com pesos não negativos. Dado um vértice de origem, ele calcula
o menor custo para alcançar todos os outros vértices do grafo.

**Estrutura de dados utilizada**
Uma fila de prioridades que sempre retira o vértice com menor
estimativa de custo atual.

**Funcionamento passo a passo**
1. Inicializa o custo da origem como 0 e todos os outros como
   infinito (-1 nesta questão)
2. Insere todos os vértices na fila de prioridades
3. Repete até a fila estar vazia:
   - Retira o vértice u com menor custo da fila
   - Para cada vizinho v de u:
     - Calcula o novo custo: custo(u) + peso(u, v)
     - Se o novo custo for menor que o custo atual de v,
       atualiza o custo de v

**Exemplo com origem D, média = 171 e desvio padrão = 10**

| Iteração | Vértice retirado | Vértices atualizados         |
|----------|-----------------|------------------------------|
| 1ª       | D (custo 0)     | A=5, B=9, E=4, F=1           |
| 2ª       | F (custo 1)     | G=2                          |
| 3ª       | E (custo 4)     | Verifica vizinhos de E       |
| ...      | ...             | ...                          |

**Complexidade**

| Implementação            | Complexidade        |
|--------------------------|---------------------|
| Com matriz de adjacência | O(V²)               |
| Com fila de prioridades  | O((V + E) log V)    |

Onde V é o número de vértices e E o número de arestas.

**Limitações**
O algoritmo de Dijkstra **não funciona** com arestas de peso
negativo. Para grafos com pesos negativos, utiliza-se o algoritmo
de Bellman-Ford.

**Ponto importante**
A cada iteração, o vértice retirado da fila é sempre aquele com
o menor custo estimado até o momento. Uma vez que um vértice é
retirado da fila, seu custo não muda mais, pois já é o mínimo
possível.

---
## Referências

- [Dijkstra's Algorithm](https://www.w3schools.com/dsa/dsa_algo_graphs_dijkstra.php)
- [Algoritmo de Dijkstra](https://www.facom.ufu.br/~madriana/ED2/6-AlgDijkstra.pdf)

---
## Questões Relacionadas

- [[Questão 34]]

---
## Conceitos Relacionados

- [[]]