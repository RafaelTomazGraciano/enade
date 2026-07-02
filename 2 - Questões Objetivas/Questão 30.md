## Questão 30

### Texto

Um compilador é um software que traduz um programa descrito em uma linguagem de alto nível para um programa equivalente em código de máquina para um processador. Em geral, um compilador não produz diretamente o código de máquina, mas sim, um programa em linguagem simbólica (*assembly*) semanticamente equivalente ao programa em linguagem de alto nível. O programa em linguagem simbólica é, então, traduzido para o programa em linguagem de máquina através de montadores. Para realizar esta tarefa, o compilador executa a análise léxica, sintática e semântica do código-fonte do programa que está sendo executado em linguagem abstrata para depois gerar o código de máquina.

> BRANCO, G. A. Jr.; TAMAE, R. Y. Uma breve introdução ao estudo e implementação de compiladores. **Revista Científica Eletrônica de Psicologia**. Ano V, n. 08, fev. 2008 (adaptado).

---

## Enunciado

Considerando as informações do texto, avalie as afirmações a seguir.

> **I.** O analisador sintático tem a função de verificar se a sequência de símbolos gerada pelo analisador léxico compõe um programa válido ou não.

> **II.** Na análise léxica, o analisador irá identificar cada símbolo que tenha significado para linguagem, gerando a mesma classificação para Java, Pascal ou outra linguagem.

> **III.** O analisador semântico utiliza o código fonte para verificar incoerências quanto ao significado das construções implementadas.

> **IV.** A fase de otimização do código procura melhorar o código intermediário, visando um código de máquina mais rápido em termos de execução.

É correto apenas o que se afirma em

- **A)** I e IV.
- **B)** II e III.
- **C)** II e IV.
- **D)** I, II e III.
- **E)** I, III e IV.

---
## Resposta

> **Letra E**

---
## Explicação

A afirmação I é verdadeira. O analisador sintático recebe como entrada os tokens (símbolos) gerados pelo analisador léxico e verifica se eles formam estruturas gramaticalmente válidas de acordo com as regras da linguagem.

A afirmação II é falsa. O analisador léxico identifica os tokens de um programa, mas a classificação desses tokens **não é a mesma** para linguagens diferentes. Cada linguagem tem suas próprias palavras reservadas, operadores e regras para identificadores. Por exemplo, `begin` é uma palavra reservada em Pascal mas não em Java. O analisador léxico é construído especificamente para a linguagem que está sendo compilada.

A afirmação III é verdadeira. O analisador semântico verifica se as construções do programa fazem sentido do ponto de vista do significado, mesmo que sejam sintaticamente corretas. Exemplos de erros semânticos incluem usar uma variável sem declarar, somar um inteiro com um booleano ou chamar uma função com número errado de argumentos.

A afirmação IV é verdadeira. Após a geração do código intermediário, a fase de otimização aplica transformações para tornar o código mais eficiente, reduzindo o número de operações, eliminando código morto e melhorando o uso de registradores, com o objetivo de gerar um código de máquina final mais rápido.

---
## Conceitos Relacionados

- [[Compiladores e Fases da Compilação]]
