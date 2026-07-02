# Pipeline
---
## Área de Estudo: Arquitetura de Computadores
---
## Explicação

Pipeline é uma técnica de arquitetura de computadores que permite
executar múltiplas instruções simultaneamente, dividindo a execução
em estágios independentes que funcionam em paralelo.

**Pipeline de 5 estágios (modelo clássico)**

| Estágio | Nome                        | Função                                      |
|---------|-----------------------------|---------------------------------------------|
| S1      | Busca de instrução (IF)     | Busca a instrução na memória/cache          |
| S2      | Decodificação (ID)          | Determina o tipo e os operandos             |
| S3      | Busca de operandos (OF)     | Localiza os operandos nos registradores     |
| S4      | Execução (EX)               | Realiza a operação                          |
| S5      | Escrita (WB)                | Grava o resultado no registrador            |

**Funcionamento**
Sem pipeline, cada instrução precisa completar todos os estágios
antes que a próxima comece. Com pipeline, enquanto a instrução 1
está no estágio S2, a instrução 2 já entra no estágio S1, e assim
por diante, aumentando muito o desempenho.

**Bolha no pipeline**
Uma bolha é uma ausência de instrução útil em um estágio. Ocorre
quando há uma falta na busca de instrução ou um desvio condicional
não resolvido. A bolha percorre todos os estágios seguintes, um por
ciclo, até ser eliminada. Em um pipeline de 5 estágios, uma bolha
criada no S1 leva 4 ciclos para ser eliminada.

**Hazards (problemas do pipeline)**
Situações que impedem a execução contínua do pipeline:
- **Hazard estrutural:** dois estágios precisam do mesmo recurso
  ao mesmo tempo
- **Hazard de dados:** uma instrução depende do resultado de outra
  que ainda não terminou
- **Hazard de controle:** instrução de desvio condicional impede
  saber qual instrução buscar a seguir

**BTB (Branch Target Buffer)**
Técnica que resolve o hazard de controle. O BTB armazena os
endereços de destino de desvios anteriores e permite prever para
onde o programa vai saltar antes que o desvio seja resolvido.
Isso permite que o pipeline continue buscando instruções sem
criar bolhas.

---
## Referências

- Livro - Organização Estruturada de Computadores (Tanenbaum)
- [Pipeline](https://ic.ufrj.br/~gabriel/arqcomp2/Pipeline.pdf)
---
## Questões Relacionadas

- [[Questão 28]]
---
## Conceitos Relacionados

- [[Arquitetura de Von Neumann]]