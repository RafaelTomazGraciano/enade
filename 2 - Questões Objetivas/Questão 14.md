## Questão 14

### Texto

O primeiro computador criado foi o ENIAC *(Electronic Numerical Integrator And Computer)*, desenvolvido por Eckert e Mauchly na Universidade da Pennsylvania, Estados Unidos. O projeto iniciou-se em 1943, financiado pelo governo americano. O período era da Segunda Guerra Mundial e o objetivo era poder calcular de forma mais ágil as melhores trajetórias para transporte de armas e mantimentos em meio aos exércitos inimigos. Esse é o tipo de cálculo que pequenos aparelhos celulares fazem hoje para encontrar rotas nas cidades por meio de GPS *(Global Positioning System)* e análise de mapa. O projeto só foi concluído em 1946, tarde demais para ser utilizado na Segunda Guerra, mas foi bastante utilizado até 1955.

Muitos projetos surgiram depois do ENIAC, mas eles eram barrados por algumas dificuldades e limitações, como por exemplo, o fato de não serem programados e trabalharem com números decimais. O problema de trabalhar com decimais é que cada algarismo armazenado possui 10 estados possíveis, representando os números de 0 a 9. Dentro de um sistema eletrônico, isso é complicado por que a carga de cada dispositivo, seja transistor, seja válvula, deveria ser medida para se verificar que número ela estava representando. Os erros eram muito frequentes. Bastava que uma válvula estivesse fora da temperatura ideal para que os resultados das operações começassem a sair errado. Von Neumann recomendou, então, que, em sua arquitetura, os dados e instruções passassem a ser armazenados em código binário, facilitando a análise dos mesmos e reduzindo a quantidade de erros.

> BRITO, A. V. **Introdução a Arquitetura de Computadores**. UFPB Virtual, 2020. Disponível em: http://producao.virtual.ufpb.br/. Acesso em: 05 maio 2020 (adaptado).

---

## Enunciado

Acerca da arquitetura de Von Neumann, avalie as asserções a seguir e a relação proposta entre elas.

> **I.** Embora as arquiteturas de computadores tenham evoluído muito do ENIAC aos modernos notebooks de hoje, a arquitetura de Von Neumann, conceito da década de 1950, tem se mantido até os dias atuais.

**PORQUE**

> **II.** A arquitetura de Von Neumann permite que a CPU realize a busca de uma ou mais instruções além da próxima a ser executada; essa técnica é utilizada para acelerar a velocidade de operação da CPU, uma vez que a próxima instrução a ser executada está normalmente armazenada nos registradores da CPU e não precisa ser buscada da memória principal, que é muito mais lenta.

A respeito dessas asserções, assinale a opção correta.

- **A)** As asserções I e II são proposições verdadeiras, e a II é uma justificativa correta da I.
- **B)** As asserções I e II são proposições verdadeiras, mas a II não é uma justificativa correta da I.
- **C)** A asserção I é uma proposição verdadeira, e a II é uma proposição falsa.
- **D)** A asserção I é uma proposição falsa, e a II é uma proposição verdadeira.
- **E)** As asserções I e II são proposições falsas.

## Resposta

> **Letra C**
## Explicação

Antes de entender o porquê de uma ser correta e a outra ser falsa, tem que se entender o que é a Arquitetura de Von Neumann

A arquitetura tem três componentes principais
1. Processador - Uma "máquina" capaz de executar instruções genéricas e processar dados
2. Memória - Onde está contido os **dados** e **código**
3. Barramento - Espaço em que dados e código chegam e saem da CPU

A arquitetura de Von Neumann é simples por natureza, ótima para produção em massa de computadores

A segunda está se referindo ao cache de instrução. Ao invés de pegar sempre da memória RAM, desloca-se um bloco de tamanho definido para o cache, assim o contador de instrução precisa checar o cache e pegar do cache, diminuindo tempo de busca.

## Conceitos Relacionados

- [[Arquitetura de Von Neumann]]
