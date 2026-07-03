# Sistemas Distribuídos

---
## Área de Estudo: Sistemas Distribuídos
---

## Explicação

Um sistema distribuído é um conjunto de computadores independentes que se apresenta ao usuário como um sistema único e coerente. Os componentes de hardware ou software, localizados em máquinas diferentes interligadas em rede, comunicam-se e coordenam suas ações **exclusivamente por troca de mensagens**, sem compartilhar memória física nem um relógio global.

### Características principais

- **Heterogeneidade:** Os dispositivos que compõem um sistema distribuído normalmente diferem em hardware, sistema operacional, linguagem de programação e protocolos de rede. O sistema distribuído deve funcionar apesar dessa diversidade, geralmente por meio de **middleware**, uma camada de software que oculta as diferenças entre as plataformas e oferece um modelo de programação uniforme.

- **Abertura:** Um sistema aberto é aquele cujos serviços seguem regras padronizadas que descrevem a sintaxe e a semântica de suas interfaces. Isso permite que novos componentes, de fabricantes diferentes, sejam adicionados e interoperem com os já existentes.

- **Escalabilidade:** É a capacidade de o sistema continuar eficiente à medida que cresce o número de usuários, de recursos ou a carga de trabalho. Um sistema escalável permite adicionar novos dispositivos (servidores, nós de processamento) para atender a uma demanda crescente ou temporária, sem exigir uma reestruturação completa da arquitetura.

- **Tratamento de falhas:** Como os componentes se comunicam apenas por mensagens em uma rede, falhas parciais são inevitáveis (um nó pode falhar enquanto outros continuam funcionando normalmente). Um sistema distribuído bem projetado deve detectar falhas, mascará-las quando possível e manter a disponibilidade do serviço mesmo com a falha de alguns componentes. Arquiteturas _peer-to-peer_, por não dependerem de um servidor central, são especialmente resilientes a esse tipo de falha, já que não existe um ponto único de falha.

- **Concorrência:** Vários clientes podem acessar e manipular o mesmo recurso compartilhado ao mesmo tempo. Esse acesso concorrente exige mecanismos de controle (como _locks_, semáforos e transações) para evitar inconsistências.

- **Transparência:** É a propriedade de esconder do usuário a natureza distribuída do sistema, fazendo-o parecer um sistema único. Existem vários tipos:

| Tipo de transparência | O que esconde                                                                     |
| --------------------- | --------------------------------------------------------------------------------- |
| Acesso                | Diferenças na representação dos dados e na forma de acessar recursos              |
| Localização           | A localização física de um recurso                                                |
| Concorrência          | O fato de o recurso estar sendo compartilhado por vários usuários simultaneamente |
| Replicação            | A existência de múltiplas cópias de um recurso                                    |
| Falha                 | Falhas e recuperação de componentes                                               |
| Mobilidade            | O deslocamento de recursos ou clientes entre diferentes locais                    |
| Desempenho            | Reconfigurações feitas para melhorar o desempenho                                 |
| Escalonamento         | O crescimento estrutural do sistema sem alterar sua arquitetura lógica            |

### Sincronização e tempo em sistemas distribuídos

Como não existe memória compartilhada nem um relógio físico global, a noção de "tempo" e de "ordem dos eventos" é um problema central. Os relógios físicos locais de cada máquina tendem a divergir ao longo do tempo (_clock drift_), por isso a coordenação de eventos costuma ser feita por meio de **relógios lógicos** (como os relógios de Lamport), que estabelecem uma ordem causal entre eventos sem depender de tempo físico sincronizado.

---
## Referências

- Livro - Sistemas distribuídos (Coulouris)
- [O que é um sistema distribuído?](https://www.atlassian.com/br/microservices/microservices-architecture/distributed-architecture)
- [Sistemas Distribuídos: Conceito e Definições](https://medium.com/sicreditech/sistemas-distribu%C3%ADdos-conceito-e-defini%C3%A7%C3%B5es-f2baa4efc88d)
- [O que são sistemas distribuídos?](https://www.ibm.com/br-pt/think/topics/distributed-systems)

---

## Questões Relacionadas

- [[Questão 35]]

---
## Conceitos Relacionados

- [[]]