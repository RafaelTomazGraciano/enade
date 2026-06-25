## Questão 18

### Texto

As técnicas de aprendizado de máquinas empregam um princípio de inferência denominado indução, no qual é possível obter conclusões genéricas a partir de um conjunto particular de exemplos. Estas técnicas de aprendizados indutivos podem ser divididas em dois principais tipos: os supervisionados e os não supervisionados. No aprendizado supervisionado é fornecida uma referência do objetivo a ser alcançado, isto é, um treinamento com o conhecimento do ambiente. Diferentemente do aprendizado supervisionado, o não supervisionado não utiliza referências, ou seja, não ocorre um treinamento com o conhecimento do ambiente.

> PELLUCCI P. R. S. *et al*. Utilização de técnicas de aprendizado de máquina no reconhecimento de entidades nomeadas no português. Belo Horizonte. **E-xacta**, v. 4, n. 1, p. 73-81, 2011 (adaptado).

---

## Enunciado

Considerando as informações do texto, avalie as afirmações a seguir.

> **I.** A regressão linear é um exemplo de modelo baseado no aprendizado supervisionado.

> **II.** A diferença entre a saída desejada e a saída gerada é o valor do erro de um aprendizado não supervisionado.

> **III.** O aprendizado não supervisionado é mais utilizado quando o entendimento dos dados é feito por meio de reconhecimento de padrões.

> **IV.** O aprendizado supervisionado é capaz de tomar decisões precisas ao receber novos dados a partir de um treinamento com dados conhecidos.

É correto apenas o que se afirma em

- **A)** I e III.
- **B)** II e III.
- **C)** II e IV.
- **D)** I, II e IV.
- **E)** I, III e IV.

---
## Resposta

> **Letra E**

---
## Explicação

A afirmação I é verdadeira. A regressão linear é um algoritmo clássico de aprendizado supervisionado. Nela, o modelo é treinado com um conjunto de exemplos que já possuem a resposta correta, e aprende a prever valores para novos dados.

A afirmação II é falsa. A diferença entre a saída desejada e a saída gerada é a definição de erro no aprendizado **supervisionado**, não no não supervisionado. No aprendizado supervisionado, existe uma resposta de referência com a qual a saída do modelo pode ser comparada. No aprendizado não supervisionado, não existe essa referência, portanto não faz sentido calcular um erro dessa forma.

A afirmação III é verdadeira. O aprendizado não supervisionado é usado justamente quando não há respostas de referência disponíveis e o objetivo é descobrir padrões, agrupamentos ou estruturas nos dados por conta própria. Exemplos comuns são algoritmos de clusterização, como o K-means.

A afirmação IV é verdadeira. O aprendizado supervisionado treina o modelo com dados cujas respostas já são conhecidas. Após o treinamento, o modelo é capaz de generalizar esse conhecimento e tomar decisões para novos dados que ainda não foram vistos.

---
## Conceitos Relacionados

- [[Tipos de Aprendizado]]