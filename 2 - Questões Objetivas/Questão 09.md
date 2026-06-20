## Questão 09

### Texto

Quando um computador é multiprogramado, ele geralmente tem múltiplos processos ou *threads* que competem pela CPU ao mesmo tempo. Essa situação ocorre sempre que dois ou mais processos estão simultaneamente no estado pronto. Se somente uma CPU se encontrar disponível, deverá ser feita uma escolha de qual processo executar em seguida. A parte do sistema operacional que faz a escolha é chamada de **escalonador**, e o algoritmo que ele usa é o **algoritmo de escalonamento**.

> TANENBAUM, A. S. **Sistemas Operacionais Modernos**. 3. ed., São Paulo: Pearson, 2010 (adaptado).

---

## Enunciado

Considerando que em ambientes diferentes são necessários algoritmos diferentes de escalonamento, garantindo assim que seja maximizado o uso de seus recursos, assinale a opção que apresenta um algoritmo de escalonamento seguido do tipo de ambiente no qual deva ser implementado.

- **A)** Primeiro a chegar, último a sair (*first in, last out* - FILO); propício para sistemas de tempo real.
- **B)** Escalonamento por taxas monotônicas (*rate monotonic scheduling* - RMS); propício para sistemas em lote.
- **C)** Tarefa mais curta primeiro; propício para sistemas interativos.
- **D)** Escalonamento por chave circular (*round-robin*); propício para sistemas de tempo real.
- **E)** Escalonamento por prioridades; propício para sistemas interativos.
---
## Resposta

> **Letra E**

---
## Explicação

A alternativa A é falsa. O algoritmo FILO (primeiro a chegar, último a sair) não existe como algoritmo de escalonamento. O algoritmo real é o FIFO (primeiro a chegar, primeiro a sair), que é propício para sistemas em lote, não para sistemas de tempo real.

A alternativa B é falsa. O RMS (escalonamento por taxas monotônicas) é um algoritmo usado especificamente em sistemas de tempo real, não em sistemas em lote. Ele atribui prioridades com base na frequência com que cada tarefa precisa ser executada.

A alternativa C é falsa. O algoritmo de tarefa mais curta primeiro é propício para sistemas em lote, pois reduz o tempo médio de espera quando se conhece antecipadamente o tempo de execução de cada processo. Em sistemas interativos, não é possível saber com precisão quanto tempo cada tarefa vai durar.

A alternativa D é falsa. O round-robin é um algoritmo baseado em fatias de tempo distribuídas igualmente entre os processos, o que o torna propício para sistemas interativos, não para sistemas de tempo real.

A alternativa E é verdadeira. O escalonamento por prioridades é adequado para sistemas interativos, pois permite que processos mais urgentes ou mais relevantes para o usuário sejam executados antes de outros, garantindo uma boa experiência para o usuário.

---
## Conceitos Relacionados

- [[Algoritmos de Escalonamento]]