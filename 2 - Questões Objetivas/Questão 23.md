## Questão 23

### Texto

O uso da estrutura de dados tipo Árvore Binária de Busca é uma técnica fundamental de programação. Uma árvore binária é um conjunto finito de elementos que está vazio ou é particionado em três subconjuntos, a saber: 1) raiz da árvore - elemento inicial (único), 2) subárvore da esquerda - se vista isoladamente compõe outra árvore e 3) subárvore da direita - se vista isoladamente compõe outra árvore. A árvore pode não ter qualquer elemento (árvore vazia). A definição de árvore é recursiva e, devido a isso, muitas operações sobre árvores binárias utilizam recursão. Sendo "A" a raiz de uma árvore binária e "B" a raiz de sua subárvore esquerda ou direita, é dito que "A" é pai de "B" e que "B" é filho de "A". Um elemento sem filhos é chamado de folha. A altura da árvore é o número de elementos encontrados no caminho descendente mais longo que liga a sua raiz até uma folha.

Uma Árvore de Busca Binária é uma árvore binária especializada, na qual a informação que o elemento filho esquerdo possui é numericamente menor que a informação do elemento pai. De forma análoga, a informação que o elemento filho direito possui é numericamente maior ou igual à informação do elemento pai. O objetivo de organizar dados em Árvores Binárias de Busca é facilitar a tarefa de encontrar um determinado elemento. O percurso completo de uma árvore binária consiste em visitar todos os elementos desta árvore, segundo algum critério, a fim de processá-los. Três formas são bem conhecidas para a realização deste percurso: 1) pré-ordem, 2) em-ordem e 3) pós-ordem. A figura a seguir mostra um exemplo de árvore binária.

![[arvore-binaria-exemplo.png]]

*Figura – Exemplo de Árvore Binária*

> LAUREANO, M. A. P. **Estrutura de Dados com Algoritmos**. São Paulo: Brasport, 2008. p. 126, 129, 136 (adaptado).

---

## Enunciado

Considerando o texto e a figura apresentados e que a seguinte lista de elementos numéricos: (27, 34, 40, 18, 23, 5, 25, 36, 10, 7, -2) seja totalmente transferida para uma estrutura de Árvore Binária de Busca, inicialmente vazia, elemento a elemento, da esquerda para a direita, assinale a alternativa correta.

- **A)** A árvore resultante terá 5 níveis de altura, com 6 elementos à esquerda da raiz principal (inicial) e 4 elementos à direita.
- **B)** O percurso da árvore em Pré-ordem irá processar os elementos na seguinte ordem (do primeiro ao último): -2, 7, 10, 5, 25, 23, 18, 36, 40, 34, 27.
- **C)** O percurso da árvore em Em-ordem irá processar os elementos na seguinte ordem (do primeiro ao último): -2, 5, 7, 10, 18, 23, 25, 27, 34, 36, 40.
- **D)** O percurso da árvore em Pós-ordem irá processar os elementos na seguinte ordem (do primeiro ao último): 27, 18, 5, -2, 10, 7, 23, 25, 34, 40, 36.
- **E)** O número máximo de elementos que essa árvore poderá ter com 10 níveis será de 1 024 elementos.
---
## Resposta

> **Letra C**

---
## Explicação

Primeiro, é necessário construir a árvore inserindo os elementos na ordem dada: (27, 34, 40, 18, 23, 5, 25, 36, 10, 7, -2).

A raiz é 27. A partir daí, cada elemento é inserido seguindo a regra: menores vão para a esquerda, maiores ou iguais vão para a direita.

```
                27
              /    \
            18      34
           /  \       \
          5   23      40
         / \    \    /
       -2  10   25  36
             \
              7
```

Com a árvore construída, é possível avaliar cada alternativa.

**Alternativa A é falsa.** A árvore tem 6 níveis de altura, não 5. Além disso, à esquerda da raiz estão: 18, 5, 23, -2, 10, 25, 7, -2, ou seja, 7 elementos, não 6.

**Alternativa B é falsa.** O percurso em pré-ordem visita os nós na ordem: raiz, subárvore esquerda, subárvore direita. A ordem correta seria: 27, 18, 5, -2, 10, 7, 23, 25, 34, 36, 40. A alternativa apresenta uma ordem invertida, como se fosse pós-ordem.

**Alternativa C é verdadeira.** O percurso em em-ordem visita os nós na ordem: subárvore esquerda, raiz, subárvore direita. Em uma Árvore Binária de Busca, o percurso em em-ordem sempre produz os elementos em ordem crescente. Como os elementos são -2, 5, 7, 10, 18, 23, 25, 27, 34, 36, 40, a alternativa está correta.

**Alternativa D é falsa.** O percurso em pós-ordem visita os nós na ordem: subárvore esquerda, subárvore direita, raiz. A raiz (27) deveria ser a última visitada, mas a alternativa a coloca como primeira.

**Alternativa E é falsa.** Uma árvore binária com N níveis pode ter no máximo 2^N - 1 elementos. Com 10 níveis, o máximo seria 2^10 - 1 = 1023 elementos, não 1024.

---
## Conceitos Relacionados

- [[Árvore Binária de Busca]]