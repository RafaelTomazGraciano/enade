## Questão 35

### Texto

Um sistema distribuído é aquele no qual os componentes de hardware ou software, localizados em computadores interligados em rede, comunicam-se e coordenam suas ações apenas enviando mensagens entre si.

> COULOURIS, G. *et al*. **Sistemas distribuídos**: conceitos e projeto. 5. ed., Porto Alegre: Bookman, 2013 (adaptado).

---

## Enunciado

Com base na definição apresentada e nos conceitos básicos de sistemas distribuídos, assinale a opção correta.

- **A)** A existência de um relógio físico local sincronizado com um relógio global é o que permite aos usuários de um sistema distribuído trocarem mensagens de forma coordenada.
- **B)** A falha de um componente em um sistema distribuído *peer-to-peer* causa a interrupção de todos os demais componentes até o seu retorno.
- **C)** O compartilhamento dos recursos distribuídos entre computadores interligados por uma rede é possível desde que os dispositivos sejam homogêneos em termos de hardware e software.
- **D)** A adição de novos dispositivos em um sistema distribuído para atender a uma demanda temporária ou crescente está ligada à característica de escalabilidade do sistema.
- **E)** A possibilidade de vários clientes acessarem de forma concorrente um mesmo recurso compartilhado em um servidor é resultado do alto nível de transparência do sistema.

---
## Resposta

> **Letra D**

---
## Explicação


- **A)** é falsa. Em sistemas distribuídos não existe um relógio global compartilhado de forma direta entre os componentes; cada máquina possui seu próprio relógio físico, e esses relógios tendem a divergir (fenômeno conhecido como _clock drift_). A coordenação entre processos distribuídos depende de mensagens e de mecanismos como relógios lógicos (por exemplo, os relógios de Lamport), não da sincronização de um relógio físico global. A troca de mensagens não depende de sincronização de relógio para acontecer.

- **B)** é falsa. Uma das principais vantagens de uma arquitetura _peer-to-peer_ é justamente a ausência de um ponto único de falha. Como não há um servidor central do qual todos dependem, a falha de um nó geralmente afeta apenas as operações que dependiam diretamente dele, e não interrompe o funcionamento de todos os demais componentes.

- **C)** é falsa. Um dos objetivos centrais dos sistemas distribuídos é justamente permitir o compartilhamento de recursos entre dispositivos **heterogêneos**, ou seja, com hardware, sistemas operacionais, linguagens de programação e redes diferentes. Middlewares e protocolos padronizados (como HTTP, TCP/IP) existem exatamente para tornar essa comunicação possível apesar da heterogeneidade, e não apenas quando os dispositivos são idênticos.

- **D)** é verdadeira. Escalabilidade é a capacidade de um sistema distribuído continuar funcionando de forma eficiente à medida que cresce, seja em número de usuários, seja em volume de recursos exigidos. Adicionar novos dispositivos para absorver uma demanda temporária ou crescente é exatamente a definição prática dessa característica: o sistema se expande (ou se retrai) sem exigir uma reestruturação completa.

- **E)** é falsa. O acesso concorrente de múltiplos clientes a um mesmo recurso é resultado do compartilhamento de recursos e de mecanismos de controle de concorrência (como _locks_ e transações), não da transparência. A transparência de concorrência, na verdade, é o que faz esse acesso simultâneo parecer invisível ou "transparente" para cada usuário individual, escondendo a existência dos demais acessos, mas não é ela que possibilita o acesso concorrente em si.

---
## Conceitos Relacionados

- [[Sistemas Distribuídos]]