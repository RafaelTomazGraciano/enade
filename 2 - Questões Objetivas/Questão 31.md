## Questão 31

### Texto

Semelhante a um autômato finito mas com uma memória ilimitada e irrestrita, uma máquina de Turing é um modelo muito mais preciso de um computador de propósito geral. Uma máquina de Turing pode fazer tudo o que um computador real pode fazer, entretanto mesmo ela não pode resolver certos problemas. Num sentido muito real, esses problemas estão além dos limites teóricos da computação.

> SIPSER, M. **Introdução à Teoria da Computação**. 2. ed. norte-americana. Cengage CTP, 2007 (adaptado).

Considere a seguinte máquina de Turing M que aceita apenas números binários palíndromos cujo comprimento é par.

**Observação:** no diagrama, as transições estão representadas no seguinte formato: "Leitura/Escrita Movimento", onde direção pode ser "D" (direita) ou "E" (esquerda). Exemplo: "0/B D" significa que o símbolo lido é "0", o símbolo escrito é "B" e o movimento é para a direita.

![[maquina-de-turing-palindromos.png]]

---

## Enunciado

Considerando que o estado inicial de M é q0, que a sua fita se encontra inicializada com a entrada 110011 e infinitos símbolos "B" à esquerda e à direita, e que a cabeça de leitura encontra-se inicialmente no símbolo mais à esquerda da entrada, avalie as afirmações a seguir.

> **I.** Após 4 movimentos de M, o conteúdo da fita, excluindo-se os símbolos "B", é "110011".

> **II.** Após 8 movimentos de M, o conteúdo da fita, excluindo-se os símbolos "B", é "1001".

> **III.** A máquina irá certamente travar em um estado de aceitação.

> **IV.** Existe um autômato com pilha que também aceita a linguagem de M.

É correto apenas o que se afirma em

- **A)** I e II.
- **B)** I e IV.
- **C)** II e III.
- **D)** I, III e IV.
- **E)** II, III e IV.

---
## Resposta

> **Letra E**

---
## Explicação

Para avaliar as afirmações, é necessário simular o funcionamento da máquina de Turing com a entrada `110011`. O diagrama mostra que a máquina funciona lendo o símbolo mais à esquerda, substituindo-o por "B", indo até o símbolo mais à direita, substituindo-o por "B", e voltando para verificar o próximo par. Esse processo verifica se a entrada é um palíndromo de comprimento par.

**Simulando os movimentos:**

Partindo de `110011` com a cabeça no primeiro "1":

- Movimentos 1 e 2: lê o "1" da esquerda, substitui por "B", move para a direita até o "1" da direita, substitui por "B". A fita fica `B1001B`.
- Movimentos 3 e 4: a cabeça retorna para a esquerda em busca do próximo símbolo não-B.

**Afirmação I é falsa.** Após 4 movimentos, os dois "1" das extremidades já foram substituídos por "B", portanto o conteúdo da fita excluindo "B" é `1001`, não `110011`.

**Afirmação II é verdadeira.** Após 8 movimentos, o primeiro par ("1" e "1") já foi verificado e apagado nos primeiros movimentos. O conteúdo da fita excluindo "B" é `1001`, confirmando que os símbolos das extremidades foram removidos.

**Afirmação III é verdadeira.** A entrada `110011` é um palíndromo binário de comprimento par (6 caracteres). Como a máquina aceita exatamente essa classe de palavras, ela irá processar todos os pares corretamente e terminar no estado de aceitação qf.

**Afirmação IV é verdadeira.** A linguagem aceita por M é a linguagem dos palíndromos binários de comprimento par. Essa é uma linguagem livre de contexto, pois pode ser descrita por uma gramática livre de contexto. Linguagens livres de contexto são reconhecidas por autômatos com pilha, portanto existe sim um autômato com pilha que aceita essa mesma linguagem.

---
## Conceitos Relacionados

- [[Máquina de Turing]]