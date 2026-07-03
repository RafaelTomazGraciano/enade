## Questão 34

### Texto

O algoritmo de Dijkstra para o problema do caminho mínimo em dígrafos com pesos utiliza uma fila de prioridades de vértices, na qual as prioridades são uma estimativa do custo final. A cada iteração, um vértice é retirado da fila, e os arcos que começam nesse vértice são analisados. Considere o seguinte grafo, no qual deseja-se conhecer o custo de um caminho mínimo para cada vértice, a partir do vértice D. Considere que -1 representa um custo "infinito", ou seja, nenhum caminho até o vértice foi até o momento descoberto.

![[grafo-dijkstra.png]]

---

## Enunciado

Com base nas informações e no grafo apresentados, assinale a alternativa que representa a estimativa de custo após duas iterações do algoritmo.

- **A)** A: 5 B: 6 C: 10 D: 0 E: 4 F: 1 G: -1
- **B)** A: 5 B: 9 C: -1 D: 0 E: 5 F: 1 G: -1
- **C)** A: 5 B: 9 C: -1 D: 0 E: 4 F: 1 G: 2
- **D)** A: 5 B: 7 C: 8 D: 0 E: 4 F: 1 G: 2
- **E)** A: 5 B: 6 C: 8 D: 0 E: 3 F: 1 G: 2

---
## Resposta

> **Letra C**

---
## Explicação

Para resolver esta questão é necessário simular as duas primeiras iterações do algoritmo de Dijkstra a partir do vértice D.

**Estado inicial:**  
Todos os vértices começam com custo -1 (infinito), exceto D que começa com 0.

```
A: -1  B: -1  C: -1  D: 0  E: -1  F: -1  G: -1
```

**Primeira iteração: vértice D é retirado da fila (menor custo = 0)**

O algoritmo analisa todos os arcos que partem de D. Com base no grafo da questão, D se conecta a:

- A com custo 5 → A recebe estimativa 0 + 5 = **5**
- B com custo 9 → B recebe estimativa 0 + 9 = **9**
- E com custo 4 → E recebe estimativa 0 + 4 = **4**
- F com custo 1 → F recebe estimativa 0 + 1 = **1**

Estado após a primeira iteração:

```
A: 5  B: 9  C: -1  D: 0  E: 4  F: 1  G: -1
```

**Segunda iteração: vértice F é retirado da fila (menor custo = 1)**

O algoritmo analisa todos os arcos que partem de F. F se conecta a:

- G com custo 1 → G recebe estimativa 1 + 1 = **2**

Nenhum outro vizinho de F oferece caminho mais curto do que o já conhecido.

Estado após a segunda iteração:

```
A: 5  B: 9  C: -1  D: 0  E: 4  F: 1  G: 2
```

---
## Conceitos Relacionados

- [[Algoritmo de Dijkstra]]