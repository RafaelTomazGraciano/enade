# Árvore Binária de Busca
---
## Área de Estudo: Estruturas de Dados
---
## Explicação

Uma Árvore Binária de Busca (ABB) é uma estrutura de dados hierárquica
em que cada nó pode ter no máximo dois filhos, seguindo a regra:
- Filho esquerdo: valor menor que o pai
- Filho direito: valor maior ou igual ao pai

**Terminologia**
- **Raiz:** nó inicial, sem pai
- **Folha:** nó sem filhos
- **Altura:** número de nós no caminho mais longo da raiz até uma folha
- **Nível:** profundidade de um nó na árvore (raiz está no nível 1)

**Inserção**
Os elementos são inseridos um a um. Cada novo elemento é comparado
com a raiz e vai para a esquerda (se menor) ou para a direita (se
maior ou igual), e o processo se repete até encontrar uma posição vazia.

**Percursos (Travessias)**

- **Pré-ordem:** Raiz → Esquerda → Direita
  Útil para copiar ou serializar a árvore.

- **Em-ordem:** Esquerda → Raiz → Direita
  Em uma ABB, sempre produz os elementos em ordem crescente.
  Esse é o percurso mais importante para provas.

- **Pós-ordem:** Esquerda → Direita → Raiz
  Útil para deletar a árvore (processa os filhos antes do pai).

**Número máximo de elementos**
Uma árvore binária com N níveis pode ter no máximo:
2^N - 1 elementos

Exemplos:
- 3 níveis → máximo de 7 elementos
- 10 níveis → máximo de 1.023 elementos

**Ponto importante**
O percurso em Em-ordem de uma ABB sempre retorna os elementos em
ordem crescente. Isso é uma consequência direta da regra de inserção
da árvore.

---
## Referências

- [Árvores binárias de busca](https://www.freecodecamp.org/portuguese/news/arvores-binarias-de-busca-bst-explicada-com-exemplos/)
---
## Questões Relacionadas

- [[Questão 23]]
---
## Conceitos Relacionados

- [[Estruturas de Dados Lineares]]