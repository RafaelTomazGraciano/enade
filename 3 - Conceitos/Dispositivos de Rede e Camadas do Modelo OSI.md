# Dispositivos de Rede e Camadas do Modelo OSI

## Área de Estudo: Redes de Computadores

## Explicação

Cada dispositivo de rede opera em uma camada diferente do modelo OSI,
e isso define quais informações ele consegue ler e como ele toma
decisões de encaminhamento.

**Camada Física**
- **Repetidor:** amplifica e regenera o sinal elétrico. Não reconhece
  quadros, pacotes ou endereços. Apenas regenera o sinal.
- **Hub:** replica o sinal recebido para todas as portas. Não possui
  buffer. Quando dois quadros chegam ao mesmo tempo, ocorre colisão.

**Camada de Enlace de Dados**
- **Bridge:** conecta segmentos de rede e isola domínios de colisão.
  Encaminha quadros apenas para a porta onde o destinatário está,
  com base no endereço MAC. Pode encaminhar vários quadros ao mesmo
  tempo.
- **Switch:** funciona como uma bridge com múltiplas portas. É o
  dispositivo mais comum em redes locais modernas.

**Camada de Rede**
- **Roteador:** examina endereços IP nos pacotes e decide o melhor
  caminho para encaminhá-los. Trabalha apenas com os protocolos
  para os quais foi configurado.

**Camada de Transporte e acima**
- **Gateway:** conecta redes ou sistemas que usam protocolos
  completamente diferentes. Um gateway de transporte, por exemplo,
  permite comunicação entre sistemas que usam TCP e SCTP.

**Resumo por camada**
| Dispositivo | Camada OSI       |           O que lê             |
|--------------|-------------------|-------------------------|
| Repetidor   | Física (1)              | Sinal elétrico               |
| Hub            | Física (1)              | Sinal elétrico               |
| Bridge        | Enlace (2)             | Endereço MAC           |
| Switch        | Enlace (2)             | Endereço MAC           |
| Roteador    | Rede (3)               | Endereço IP                |
| Gateway     | Transporte+ (4+) | Protocolo completo   |

**Ponto importante para provas**
Quanto mais alta a camada em que o dispositivo opera, mais inteligente
ele é e mais informações consegue interpretar, mas também mais lento
e caro tende a ser.

## Referências

- Livro - Redes de Computadores (Tanenbaum)
- [Rede de computadores](https://www.alura.com.br/artigos/rede-de-computadores)
- [O que é rede de computadores?](https://www.ibm.com/br-pt/think/topics/networking)

## Questões Relacionadas

- [[Questão 21]]

## Conceitos Relacionados

- [[]]