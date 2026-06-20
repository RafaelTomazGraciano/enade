# Propriedades de Proposições
---
## Área de Estudo: IA e Sistemas Digitais
---
## Explicação

As proposições de lógica, podem ter propriedades únicas de acordo com o resultado de seu tabela verdade, sendo estas as tautologias, contradições e contingencia.

---
### Tautologia
Tautologia são proposições que sempre terão Verdadeiro (V ou T ou 1) como resultado
#### Exemplo
Considere a proposição: "Chove ou não chove", modelando matematicamente, em que p representa se choveu
$$
p \lor \neg p
$$
Ao montar a tabela-verdade obtemos:

| $p$ | $\neg p$ | $p \lor \neg p$ |
| --- | -------- | --------------- |
| F   | V        | V               |
| V   | F        | V               |
Todas as linhas são verdadeiras, até podemos assumir então que
$$
\text{V} \equiv p \lor \neg p
$$
### Contradição
Contradição são proposições que sempre terão Falso (F ou 0) como resultado

#### Exemplo
Considera a proposição:  "Chove e não chove", modelando matematicamente, em que p representa se choveu
$$
p \land \neg p
$$
Ao montar a tabela-verdade obtemos:

| $p$ | $\neg p$ | $p \land \neg p$ |
| --- | -------- | ---------------- |
| F   | V        | F                |
| V   | F        | F                |
Todas as linhas são falsas, até podemos assumir então que

$$
\text{F} \equiv p \land \neg p
$$
### Contingencia
Contingencia são proprosições incertas, em que se depende de entrada externa para inferir o resultado
#### Exemplo
Considera a proposição:  "Se chover então a terra fica molhada", modelando matematicamente, em que p representa se choveu e q se a terra está molhada
$$
p \rightarrow q
$$
Ao montar a tabela-verdade obtemos:

| $p$ | $q$ | $p \rightarrow q$ |
| --- | --- | ----------------- |
| F   | F   | V                 |
| F   | V   | V                 |
| V   | F   | F                 |
| V   | V   | V                 |
Note que não podemos afirmar se a terra está molhada quando não acontece chuva, pois a única certeza que tem é que se chover a terra tem que ficar molhada, porém se não chover outra coisa pode ter deixado ela molhada (como um regador)

---
## Referências

- RUSSELL, S.; NORVIG, P. **Inteligência Artificial - Uma Abordagem Moderna**. 3. ed. New Jersey: Pearson, 2010.

---
## Questões Relacionadas

- [[Questão 3]]

## Conceitos relacionados

- [[Indução]]