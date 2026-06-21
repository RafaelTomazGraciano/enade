# Arquitetura de Von Neumann
---
## Área de Estudo: Arquitetura de Computadores
---
## Explicação

![[maquina-von-neumann.png]]

A arquitetura de Von Neumann foi proposta por John von Neumann
como solução para os problemas dos computadores da época, que não eram
programáveis e trabalhavam com números decimais, o que gerava muitos
erros. A principal inovação foi armazenar dados e instruções juntos na
mesma memória, em código binário.

### Componentes principais

- **CPU (Unidade Central de Processamento):** composta pela Unidade
  Lógica e Aritmética (ULA), responsável pelos cálculos, e pela
  Unidade de Controle (UC), responsável por buscar e interpretar
  as instruções
- **Memória:** armazena tanto os dados quanto as instruções do programa
  no mesmo espaço. Esse é o conceito de **programa armazenado**, o
  ponto central da arquitetura
- **Barramento:** canal de comunicação por onde dados e instruções
  trafegam entre a CPU e a memória
- **Dispositivos de Entrada e Saída:** permitem a comunicação do
  computador com o mundo externo

### Conceito de programa armazenado

Antes de Von Neumann, os computadores precisavam ser reconfigurados
fisicamente para executar tarefas diferentes. Com a arquitetura de Von
Neumann, o programa passa a ser armazenado na memória como dados, e a
CPU simplesmente lê e executa instrução por instrução. Isso tornou os
computadores muito mais fáceis de programar.

###  Gargalo de Von Neumann

Uma limitação conhecida da arquitetura é que a CPU e a memória se
comunicam por um único barramento. Como a CPU processa dados muito mais
rápido do que a memória consegue fornecê-los, a CPU frequentemente fica
ociosa esperando os dados chegarem. Essa limitação é chamada de
**gargalo de Von Neumann**. Tecnologias comocache e pipeline foram 
criadas para minimizar esse problema, mas não
fazem parte da arquitetura original.

### Importante

A arquitetura de Von Neumann não prevê cache nem busca antecipada de
instruções. Essas são otimizações modernas que foram adicionadas posteriormente. 

---
## Referências

- Livro - Organização Estruturada de Computadores (Tanenbaum)
- https://embarcados.com.br/arquitetura-de-john-von-neumann/

---
## Questões Relacionadas

- [[Questão 14]]

---
## Conceitos Relacionados

- [[]]