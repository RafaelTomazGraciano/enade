# Compiladores e Fases da Compilação
---
## Área de Estudo: Linguagens Formais e Compiladores
---
## Explicação

Um compilador é um software que traduz um programa escrito em uma
linguagem de alto nível para código de máquina. Esse processo ocorre
em fases sequenciais.

**Fases da compilação**

**1. Análise Léxica**
- É a primeira fase do compilador
- Lê o código-fonte caractere por caractere e agrupa os caracteres
  em unidades chamadas tokens (palavras reservadas, identificadores,
  operadores, literais)
- Cada linguagem tem suas próprias regras léxicas, portanto a
  classificação dos tokens não é a mesma para linguagens diferentes
- Exemplo: `int x = 10;` gera os tokens: `int`, `x`, `=`, `10`, `;`

**2. Análise Sintática**
- Recebe os tokens gerados pela análise léxica
- Verifica se a sequência de tokens forma estruturas gramaticalmente
  válidas de acordo com as regras da linguagem
- Gera uma árvore sintática que representa a estrutura do programa
- Detecta erros como parênteses não fechados ou comandos malformados

**3. Análise Semântica**
- Verifica o significado das construções do programa
- Detecta erros que são sintaticamente corretos mas semanticamente
  inválidos, como:
  - Usar variável sem declarar
  - Operações entre tipos incompatíveis
  - Chamar função com número errado de argumentos

**4. Geração de Código Intermediário**
- Produz uma representação intermediária do programa, independente
  da arquitetura alvo

**5. Otimização de Código**
- Aplica transformações no código intermediário para torná-lo mais
  eficiente
- Elimina código morto, reduz operações redundantes e melhora o uso
  de registradores
- Objetivo: gerar um código de máquina final mais rápido

**6. Geração de Código de Máquina**
- Traduz o código intermediário otimizado para instruções específicas
  do processador alvo

---
## Referências

- [Fases de um compilador](https://www.geeksforgeeks.org/compiler-design/phases-of-a-compiler/)
- [O que é um compilador?](https://www.ibm.com/br-pt/think/topics/compiler)
---
## Questões Relacionadas

- [[Questão 30]]
---
## Conceitos Relacionados

- [[]]