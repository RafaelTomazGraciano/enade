## Questão 17

### Texto

Durante parte do tempo, um processo está ocupado realizando computações internas e outras coisas que não levam a condições de corrida. No entanto, às vezes, um processo tem de acessar uma memória compartilhada ou arquivos, ou realizar outras tarefas críticas que podem levar a corridas. Essa parte do programa onde a memória compartilhada é acessada é chamada de **região crítica** ou **seção crítica**. Se conseguíssemos arranjar as coisas de maneira que dois processos jamais estivessem em suas regiões críticas ao mesmo tempo, poderíamos evitar as corridas. Embora essa exigência evite as condições de corrida, ela não é suficiente para garantir que processos em paralelo cooperem de modo correto e eficiente usando dados compartilhados. Precisamos que quatro condições se mantenham para chegar a uma boa solução.

1. Dois processos jamais podem simultaneamente estar dentro de suas regiões críticas.
2. Nenhuma suposição pode ser feita a respeito de velocidades ou de número de CPUs.
3. Nenhum processo executando fora de sua região crítica pode bloquear qualquer processo.
4. Nenhum processo deve ser obrigado a esperar eternamente para entrar em sua região crítica.

Em um sentido abstrato, o comportamento que queremos é mostrado na figura a seguir.

![[exclusao-mutua-regioes-criticas.png]]

*Figura - Exclusão mútua usando regiões críticas*

> TANENBAUM, A. S. **Sistemas Operacionais Modernos**. 4. ed. Versão para Biblioteca Virtual Pearson. São Paulo: Pearson Education do Brasil, p. 83, 2016 (adaptado).

---

## Enunciado

Considerando o texto e a figura apresentados, avalie as asserções a seguir e a relação proposta entre elas.

> **I.** Em algumas situações, a exclusão mútua pode ser obtida por meio da desabilitação da interrupção controlada pelo Sistema Operacional, não sendo permitido que o seu controle seja feito pelo usuário.

**PORQUE**

> **II.** A desabilitação da interrupção é uma técnica que pode impedir que o processador que está executando um processo em sua região crítica seja interrompido para executar outro código, sendo mais eficiente em sistemas de multiprocessadores devido a quantidade de processos concorrentes.

A respeito dessas asserções, assinale a opção correta.

- **A)** As asserções I e II são proposições verdadeiras, e a II é uma justificativa correta da I.
- **B)** As asserções I e II são proposições verdadeiras, mas a II não é uma justificativa correta da I.
- **C)** A asserção I é uma proposição verdadeira, e a II é uma proposição falsa.
- **D)** A asserção I é uma proposição falsa, e a II é uma proposição verdadeira.
- **E)** As asserções I e II são proposições falsas.

---
## Resposta

> **Letra C**

---
## Explicação

A asserção I é verdadeira. A desabilitação de interrupções é uma técnica real e conhecida para obter exclusão mútua. A ideia é se o processo desabilita todas as interrupções antes de entrar na região crítica e as reabilita ao sair, nenhum outro processo consegue tomar o controle da CPU nesse intervalo. Porém, como essa técnica dá ao processo um poder muito grande sobre o sistema, o controle dela é restrito ao Sistema Operacional e não pode ser feito por processos de usuário.

A asserção II é falsa. A afirmação diz que a desabilitação de interrupções é mais eficiente em sistemas **multiprocessadores**. Na verdade é o contrário, essa técnica é eficiente apenas em sistemas com um **único processador**. Em sistemas multiprocessadores, desabilitar a interrupção de uma CPU não impede que outro processador acesse a mesma região crítica ao mesmo tempo, tornando a técnica ineficaz nesses ambientes.

---
## Conceitos Relacionados

- [[Exclusão Mútua e Regiões Críticas]]