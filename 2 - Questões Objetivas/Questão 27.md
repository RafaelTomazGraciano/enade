## Questão 27

### Texto

A figura a seguir mostra o histograma de uma amostra composta de 20 000 servidores. O eixo x apresenta a quantidade de requisições simultâneas desses servidores. Por exemplo, o valor 168 indica que há 1 850 servidores com capacidade de atender 168 requisições simultâneas.

![[histograma-servidores-requisicoes.png]]

| Média         | 171 |
| ------------- | --- |
| Desvio Padrão | 10  |

> Disponível em: http://www.openintro.org. Acesso em: 05 set. 2021 (adaptado).

---

## Enunciado

É possível afirmar que ao conectarmo-nos a um servidor dessa amostra, ao acaso, há aproximadamente

- **A)** 34,13% de chance que sua capacidade esteja no intervalo [141, 201].
- **B)** 34,13% de chance que sua capacidade esteja no intervalo [161, 181].
- **C)** 76,68% de chance que sua capacidade esteja no intervalo [171, 191].
- **D)** 95,44% de chance que sua capacidade esteja no intervalo [151, 191].
- **E)** 99,74% de chance que sua capacidade esteja no intervalo [161, 181].

---
## Resposta

> **Letra D**

---
## Explicação

O histograma apresenta um formato simétrico em forma de sino, o que caracteriza uma **distribuição normal**. Com média 171 e desvio padrão 10, a regra empírica estabelece que:

- **68,26%** dos dados estão no intervalo de **1 desvio padrão** da média: [161, 181]
- **95,44%** dos dados estão no intervalo de **2 desvios padrão** da média: [151, 191]
- **99,74%** dos dados estão no intervalo de **3 desvios padrão** da média: [141, 201]

Além disso, como a distribuição é simétrica, metade de cada intervalo fica de cada lado da média:

- **34,13%** dos dados estão entre a média e 1 desvio padrão acima: [171, 181]
- **34,13%** dos dados estão entre a média e 1 desvio padrão abaixo: [161, 171]

Com isso é possível avaliar cada alternativa:

A alternativa A é falsa. O intervalo [141, 201] corresponde a 3 desvios padrão da média (171 ± 30), que abrange 99,74% dos dados, não 34,13%.

A alternativa B é falsa. O intervalo [161, 181] corresponde a 1 desvio padrão completo da média (171 ± 10), que abrange 68,26% dos dados, não 34,13%. O valor de 34,13% corresponderia apenas a metade desse intervalo.

A alternativa C é falsa. O intervalo [171, 191] vai da média até 2 desvios padrão acima, abrangendo apenas metade direita de 2 desvios padrão, o que corresponde a 47,72% dos dados, não 76,68%.

A alternativa D é verdadeira. O intervalo [151, 191] corresponde a 2 desvios padrão da média (171 ± 20), que abrange exatamente 95,44% dos dados.

A alternativa E é falsa. O intervalo [161, 181] corresponde a 1 desvio padrão da média (171 ± 10), que abrange 68,26% dos dados, não 99,74%.

---
## Conceitos Relacionados

- [[Distribuição Normal e Regra Empírica]]