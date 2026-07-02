## Questão 32

### Texto

Existe um grande número de implementações para algoritmos de ordenação. Um dos fatores a serem considerados, por exemplo, é o número máximo e médio de comparações que são necessárias para ordenar um vetor com n elementos. Diz-se também que um algoritmo de ordenação é estável se ele preserva a ordem de elementos que são iguais. Isto é, se tais elementos aparecem na sequência ordenada na mesma ordem em que estão na sequência inicial. Analise o algoritmo abaixo, onde A é um vetor e "i, j, lo e hi" são índices do vetor:

```
algoritmo ordena(A, lo, hi)
    se lo < hi então
        p := particao(A, lo, hi)
        ordena(A, lo, p - 1)
        ordena(A, p + 1, hi)


algoritmo particao(A, lo, hi)
    pivot := A[hi]
    i := lo
    repita para j := lo até hi
        se A[j] < pivot entao
        troca A[i] com A[j]
        i := i + 1
    troca A[i] com A[hi]
    return i
```

---

## Enunciado

Com relação ao algoritmo apresentado, avalie as afirmações a seguir.

> **I.** O algoritmo precisa de um espaço adicional O(n) para a pilha de recursão.

> **II.** O algoritmo apresentado é um algoritmo de ordenação recursivo e estável.

> **III.** O algoritmo precisa, em média, de O(n log n) comparações para ordenar n itens.

> **IV.** O uso do primeiro elemento do vetor como "pivot" é mais eficiente que usar o último.

É correto apenas o que se afirma em

- **A)** I e III.
- **B)** II e IV.
- **C)** III e IV.
- **D)** I, II e III.
- **E)** I, II e IV.

---
## Resposta

> **Letra A**

---
## Explicação

O algoritmo apresentado é o **Quicksort**. É possível identificá-lo pela função `particao`, que escolhe um pivot (neste caso o último elemento do vetor), reorganiza os elementos menores à esquerda e os maiores à direita, e então chama a si mesmo recursivamente para cada metade.

**Afirmação I é verdadeira.** O Quicksort é recursivo e utiliza a pilha de chamadas do sistema para armazenar os estados de cada chamada recursiva. No pior caso, quando o vetor já está ordenado e o pivot é sempre o último elemento, a recursão pode atingir n níveis de profundidade, exigindo O(n) de espaço adicional na pilha.

**Afirmação II é falsa.** O algoritmo é de fato recursivo, mas **não é estável**. A instabilidade ocorre porque a função `particao` realiza trocas de elementos distantes entre si, o que pode alterar a ordem relativa de elementos com valores iguais. Por exemplo, se dois elementos iguais existirem no vetor, a troca pode inverter a posição em que apareciam originalmente.

**Afirmação III é verdadeira.** No caso médio, o Quicksort realiza O(n log n) comparações. Isso ocorre quando o pivot divide o vetor em duas partes aproximadamente iguais a cada chamada recursiva, resultando em **log n** níveis de recursão com n comparações em cada nível. No pior caso a complexidade é O(n²).

**Afirmação IV é falsa.** A escolha do primeiro ou do último elemento como pivot não garante maior eficiência. Na verdade, ambas as escolhas são igualmente ruins no pior caso, que ocorre justamente quando o vetor já está ordenado. Estratégias mais eficientes incluem escolher o pivot como a mediana de três elementos ou de forma aleatória.

---
## Conceitos Relacionados

- [[]]