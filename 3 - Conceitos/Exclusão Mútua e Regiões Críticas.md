# Exclusão Mútua e Regiões Críticas

## Área de Estudo: Sistemas Operacionais

## Explicação

Em sistemas multitarefa, vários processos competem pelo uso da CPU
e podem compartilhar recursos como memória e arquivos. Quando dois
processos acessam e modificam um recurso compartilhado ao mesmo tempo,
podem ocorrer **condições de corrida**, gerando resultados incorretos e
imprevisíveis.

**Região Crítica**
É a parte do código de um processo em que ele acessa recursos
compartilhados. Para evitar condições de corrida, nunca dois processos
podem estar em suas regiões críticas ao mesmo tempo.

**Quatro condições para uma boa solução de exclusão mútua**
1. Dois processos jamais podem estar simultaneamente em suas regiões
   críticas
2. Nenhuma suposição pode ser feita sobre velocidade ou número de CPUs
3. Nenhum processo fora de sua região crítica pode bloquear outro
4. Nenhum processo deve esperar eternamente para entrar em sua região
   crítica

**Técnicas de exclusão mútua**

- **Desabilitação de interrupções:** o processo desabilita todas as
  interrupções antes de entrar na região crítica e as reabilita ao
  sair. Funciona apenas em sistemas com **um único processador**. Em
  sistemas multiprocessadores, não é eficaz pois outros processadores
  continuam acessando a memória compartilhada. O controle dessa técnica
  é restrito ao Sistema Operacional.

- **Variáveis de travamento (lock):** uma variável compartilhada indica
  se a região crítica está ocupada ou não. Simples, mas pode gerar
  problemas de corrida na própria verificação da variável.

- **Semáforos:** mecanismo mais robusto que usa operações atômicas para
  controlar o acesso à região crítica, funcionando tanto em sistemas
  com um quanto com múltiplos processadores.

## Referências

- Livro - Sistemas Operacionais Modernos (Tanenbaum)
- [O PROBLEMA DA EXCLUSÃO MÚTUA](http://www.inf.ufrgs.br/~asc/livro/cap4-14.pdf)

## Questões Relacionadas

- [[Questão 17]]

## Conceitos Relacionados

- [[Algoritmos de Escalonamento]]