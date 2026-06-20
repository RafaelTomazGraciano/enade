## Questão 10

### Texto

A biblioteca de coleções da linguagem Java disponibiliza implementações de propósito geral para estruturas de dados elementares, como listas, filas e pilhas. Considere as seguintes definições de classes que representam implementações de estruturas de dados disponíveis na biblioteca da linguagem:

- **Classe A:** os objetos são organizados em uma ordem linear e podem ser inseridos somente no início ou no final dessa sequência;
- **Classe B:** os objetos são organizados em uma ordem linear determinada por uma referência ao próximo objeto;
- **Classe C:** os objetos são removidos na ordem oposta em que foram inseridos;
- **Classe D:** os objetos são inseridos e removidos respeitando a seguinte regra: o elemento a ser removido é sempre aquele que foi inserido primeiro.

---

## Enunciado

Nesse contexto, assinale a alternativa que representa, respectivamente, as estruturas de dados implementadas pelas classes A, B, C e D.

- **A)** Lista circular, lista simplesmente ligada, pilha e fila.
- **B)** Deque, lista simplesmente ligada, pilha e fila.
- **C)** Lista duplamente ligada, lista simplesmente ligada, fila e pilha.
- **D)** Pilha, fila, deque e lista simplesmente encadeada.
- **E)** Deque, pilha, lista ligada e fila.
---
## Resposta

> **Letra B**

---
## Explicação

A Classe A descreve uma estrutura em que objetos podem ser inseridos somente no início ou no final da sequência. É um **Deque** (Double Ended Queue), que permite inserção e remoção nas duas extremidades.

A Classe B descreve objetos organizados em ordem linear com referência ao próximo objeto. Essa é a definição de uma **lista simplesmente ligada**, onde cada elemento aponta para o próximo da sequência.

A Classe C descreve objetos removidos na ordem oposta à inserção, ou seja, o último a entrar é o primeiro a sair. Essa é a definição de uma **pilha**, que segue o princípio LIFO (Last In, First Out).

A Classe D descreve objetos em que o primeiro a entrar é o primeiro a sair. Essa é a definição de uma **fila**, que segue o princípio FIFO (First In, First Out).

---
## Conceitos Relacionados

- [[Estruturas de Dados Lineares]]