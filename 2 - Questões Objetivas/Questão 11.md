## Questão 11

### Texto

Uma equipe de cientistas da computação de uma determinada empresa de animação foi designada para desenvolver um sistema capaz de varrer a web no intuito de detectar sites que possam estar usando imagens de seus personagens de animação sem o devido consentimento. Portanto, o sistema deverá receber imagens como entrada, classificá-las entre imagens da empresa e imagens não produzidas pela empresa.

A figura abaixo esboça uma arquitetura de rede neural profunda e o processo de treinamento que os cientistas pretendem usar.

![[rede-neural-profunda.png]]

> CHOLLET, F. **Deep Learning with Python**. New York: Manning Publications, 2017 (adaptado).

Após uma tentativa, notaram-se duas dificuldades: 1) o tempo de treinamento da rede estava muito longo e 2) a acurácia da rede treinada não estava no patamar aceito pela empresa.

---

## Enunciado

Diante deste contexto, avalie as afirmações a seguir.

> **I.** Aumentar o número de camadas é uma alternativa que pode levar a uma melhora na acurácia, além de diminuir o tempo de treinamento da rede.

> **II.** Fazer uso de redes convolucionais é uma alternativa que pode levar a uma melhora na acurácia, no entanto, pode exigir uso de máquinas com maior poder de processamento.

> **III.** Aumentar o número de unidades de processamento (neurônios) nas camadas pode levar a uma piora na acurácia, além de diminuir o tempo de treinamento da rede.

> **IV.** Aumentar o número de amostras de treinamento é uma alternativa que pode levar a uma melhora na acurácia, apesar de aumentar o tempo de treinamento da rede.

> **V.** Fazer uso de redes recorrentes é uma alternativa que pode levar a uma melhora na acurácia, no entanto, pode exigir uso de máquinas com maior poder de processamento.

É correto apenas o que se afirma em

- **A)** I e IV.
- **B)** I e V.
- **C)** II e III.
- **D)** II e IV.
- **E)** III e V.

---
## Resposta

> **Letra D**

---
## Explicação

A afirmação I é falsa. Aumentar o número de camadas pode melhorar a acurácia, mas tende a **aumentar** o tempo de treinamento, não diminuí-lo. Uma rede com mais camadas tem mais parâmetros para ajustar, o que exige mais processamento a cada ciclo de treinamento.

A afirmação II é verdadeira. Redes convolucionais são especialmente projetadas para classificação de imagens, pois conseguem identificar padrões visuais de forma muito eficiente, melhorando a acurácia. Porém, exigem maior poder computacional para serem treinadas.

A afirmação III é falsa. Aumentar o número de neurônios nas camadas tende a **melhorar** a acurácia (até certo ponto), e não piorá-la. Além disso, mais neurônios significam mais processamento, o que **aumenta** o tempo de treinamento, e não o diminui.

A afirmação IV é verdadeira. Mais amostras de treinamento fornecem ao modelo mais exemplos para aprender, o que geralmente melhora a acurácia. Porém, processar um volume maior de dados exige mais tempo de treinamento.

A afirmação V é falsa. Redes recorrentes são projetadas para dados sequenciais, como texto e áudio, e não para classificação de imagens. Usá-las neste contexto não seria a escolha adequada para melhorar a acurácia do sistema descrito.

---
## Conceitos Relacionados

- [[Redes Neurais e Deep Learning]]