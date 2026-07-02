# Máquina de Turing 
---
## Área de Estudo: Teoria da Computação 
---
## Explicação

A Máquina de Turing é um modelo matemático abstrato que representa
o limite do que pode ser computado. Foi proposta por Alan Turing em 1936
e é composta por:

- **Fita infinita:** dividida em células, cada uma contendo um símbolo
- **Cabeça de leitura/escrita:** lê e escreve símbolos na fita e se
  move para a esquerda ou direita
- **Conjunto de estados:** incluindo um estado inicial e estados de
  aceitação e rejeição
- **Função de transição:** define o que fazer (escrever, mover) com
  base no estado atual e no símbolo lido

**Formato das transições**
As transições são escritas como: `símbolo lido / símbolo escrito direção`

Exemplo: `0/B D` significa:
- Leu: 0
- Escreveu: B
- Moveu: para a direita

**Hierarquia de Chomsky**
A teoria da computação classifica as linguagens em quatro tipos,
cada um reconhecido por um modelo de autômato diferente:

| Tipo | Linguagem              | Autômato reconhecedor     |
|------|------------------------|---------------------------|
| 3    | Regular                | Autômato Finito           |
| 2    | Livre de Contexto      | Autômato com Pilha        |
| 1    | Sensível ao Contexto   | Autômato Linearmente Limitado |
| 0    | Recursivamente Enumerável | Máquina de Turing      |

**Palíndromos e autômatos com pilha**
A linguagem dos palíndromos binários de comprimento par é uma
linguagem livre de contexto (Tipo 2). Isso significa que ela pode
ser reconhecida por um autômato com pilha, não sendo necessária
uma Máquina de Turing para reconhecê-la. A Máquina de Turing da questão é apenas
uma das formas possíveis de reconhecer essa linguagem.

**Ponto importante**
Toda linguagem regular também é livre de contexto, e toda linguagem
livre de contexto também é reconhecida por uma Máquina de Turing.
A hierarquia é inclusiva: cada classe contém todas as classes abaixo
dela.

## Referências

- [Máquina de Turing - Apostila](https://wwwp.fc.unesp.br/~simonedp/zipados/TC04.pdf)
- [Máquina de Turing](https://www.ufrgs.br/alanturingbrasil2012/Maquina_de_Turing.pdf)
- [Linguagens Formais](http://wiki.icmc.usp.br/images/a/a5/Aula14_4out_TiposGramaticas.pdf)

## Questões Relacionadas

- [[Questão 31]]

## Conceitos Relacionados

- [[]]