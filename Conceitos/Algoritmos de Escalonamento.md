# Algoritmos de Escalonamento
---

## Área de Estudo: Sistemas Operacionais
---
## Explicação

O escalonador é a parte do sistema operacional responsável por decidir qual processo será executado pela CPU em cada momento. O algoritmo que ele usa é chamado de algoritmo de escalonamento.

Os algoritmos variam conforme o tipo de ambiente:

**Sistemas em lote** - processam tarefas sem interação do usuário, priorizando eficiência:
- FIFO (First In, First Out): o primeiro processo a chegar é o primeiro a ser executado
- Tarefa mais curta primeiro (SJF): executa primeiro o processo com menor tempo estimado de execução

**Sistemas interativos** - precisam responder rapidamente ao usuário:
- Round-robin: cada processo recebe uma fatia de tempo igual e rotativa
- Escalonamento por prioridades: processos com maior prioridade são executados antes

**Sistemas de tempo real** - precisam garantir que tarefas sejam concluídas dentro de prazos rígidos:
- RMS (Rate Monotonic Scheduling): atribui prioridades com base na frequência de execução de cada tarefa
---
## Referências

- Livro - Sistemas Operacionais Modernos (Tanenbaum)
- [Escalonamento de processos](https://pt.wikipedia.org/wiki/Escalonamento_de_processos)
- [CPU Scheduling in Operating Systems](https://www.geeksforgeeks.org/operating-systems/cpu-scheduling-in-operating-systems/)
---
## Questões Relacionadas

- [[Questão 09]]
---
## Conceitos Relacionados

- [[]]