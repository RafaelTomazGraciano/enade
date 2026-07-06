# Questão 5

## Enunciado

Um heap binário é um arranjo que pode ser visualizado como uma árvore binária, sendo que cada nó da árvore corresponde a um elemento do arranjo, como pode ser observado na figura a seguir.

![[heap.png]]

Percebe-se que existem dois tipos de heaps: heaps máximo e heaps mínimo. O heap máximo é uma estrutura de dados que possibilita a consulta ou extração de forma eficiente do maior elemento de uma coleção. A propriedade de heap máximo especifica que um nó filho (no código calculado pelas funções left e right) tem sempre armazenado um valor menor ou igual ao seu pai.

> CORMEN, T. H.; LEISERSON, C. E.; RIVEST, R. L.; STEIN, C. **Introduction to Algorithms**. 3. ed. MIT Press and McGraw-Hill. p. 131-161, 2009 (adaptado).

Considerando a implementação a seguir, o heapify é uma função auxiliar para reorganizar o arranjo (garantindo a propriedade de heap máximo em uma determinada posição do arranjo) e buildHeap é uma função que usa heapify para reorganizar todas as posições do arranjo (garantindo a propriedade de heap máximo para todos os elementos).

```C
int left(int i) { return (2 * i + 1); }
int right(int i) { return (2 * i + 2); }
/* a - arranjo, n - número de elementos, i - posição do elemento que deve ser colocado em propriedade de heap */
void heapify (int *a, int n, int i)
{
	int e, d, max, aux;
	e = left(i);
	d = right(i);
	if (e < n && a[e] > a[i])
		max = e;
	else
		max = i;
	if (d < n && a[d] > a[max])
	max = d;
	if (max != i)
	{
	aux = a[i];
	a[i] = a[max];
	a[max] = aux;
	heapify(a, n, max);
	}
}

/*a - arranjo, n - número de elementos */
void buildHeap(int *a, int n) {
	int i;
	for (i = (n-1)/2; i >= 0; i--)
	heapify(a, n, i);
}
```

De acordo com as informações apresentadas, faça o que se pede nos itens a seguir.

a) Como ficará o arranjo `int a[] = {2, 5, 8 ,13, 21, 1, 3, 34}` após a execução da função `buildHeap(a, 8)`. b) Apresente a complexidade de tempo no pior caso para a função `heapify`, use a notação $O$ ou $\Theta$.

---

## Sugestão de Resposta

a) O respondente deve mostrar que após a execução da função buildHeap o arranjo ficará da seguinte forma: {34, 21, 8, 13, 2, 1, 3, 5}. b) O respondente deve apresentar que no pior caso para a função heapify a complexidade de tempo ficará da seguinte forma: O(log n), sendo n o número de elementos do heap.

---

## Resposta

a) Após a execução de `buildHeap(a, 8)`, o arranjo `a[] = {2, 5, 8, 13, 21, 1, 3, 34}` fica:

$$ a = {34,\ 21,\ 8,\ 13,\ 2,\ 1,\ 3,\ 5} $$

|0|1|2|3|4|5|6|7|
|---|---|---|---|---|---|---|---|
|34|21|8|13|2|1|3|5|

b) No pior caso, a complexidade de tempo da função `heapify` é:

$$ O(\log n) $$

(também podendo ser expressa como $\Theta(\log n)$), sendo $n$ o número de elementos do heap.

---

## Explicação

### a) Rastreamento de `buildHeap(a, 8)`

**Arranjo inicial (índices 0 a 7):**

|0|1|2|3|4|5|6|7|
|---|---|---|---|---|---|---|---|
|2|5|8|13|21|1|3|34|

`buildHeap` percorre `i` de `(n-1)/2 = 3` até `0`, chamando `heapify(a, n, i)` em cada posição (de baixo para cima, garantindo que as subárvores já estejam organizadas antes de tratar o nó pai).

**Passo i = 3**

- `left(3) = 7` → `a[7] = 34`; `right(3) = 8` (fora do arranjo).
- `a[3] = 13 < a[7] = 34` → `max = 7` → troca `a[3]` e `a[7]`.
- Resultado: `{2, 5, 8, 34, 21, 1, 3, 13}`
- `heapify` recursivo em `i=7`: não tem filhos, encerra.

**Passo i = 2**

- `left(2) = 5` → `a[5]=1`; `right(2) = 6` → `a[6]=3`.
- `a[2] = 8` já é maior que ambos → nenhuma troca.
- Resultado: `{2, 5, 8, 34, 21, 1, 3, 13}` (inalterado)

**Passo i = 1**

- `left(1) = 3` → `a[3]=34`; `right(1) = 4` → `a[4]=21`.
- `a[1] = 5 < 34` → `max = 3`. Como `21 < 34`, `max` permanece `3`.
- Troca `a[1]` e `a[3]`.
- Resultado: `{2, 34, 8, 5, 21, 1, 3, 13}`
- `heapify` recursivo em `i=3`: `left(3)=7 → a[7]=13`; `right(3)=8` (fora).
    - `a[3]=5 < a[7]=13` → troca.
    - Resultado: `{2, 34, 8, 13, 21, 1, 3, 5}`
    - `heapify` em `i=7`: sem filhos, encerra.

**Passo i = 0**

- `left(0) = 1` → `a[1]=34`; `right(0) = 2` → `a[2]=8`.
- `a[0] = 2 < 34` → `max = 1`.
- Troca `a[0]` e `a[1]`.
- Resultado: `{34, 2, 8, 13, 21, 1, 3, 5}`
- `heapify` recursivo em `i=1`: `left(1)=3 → a[3]=13`; `right(1)=4 → a[4]=21`.
    - `a[1]=2 < 13` → `max=3`; depois `21 > 13` → `max=4`.
    - Troca `a[1]` e `a[4]`.
    - Resultado: `{34, 21, 8, 13, 2, 1, 3, 5}`
    - `heapify` em `i=4`: `left(4)=9` (fora), encerra.

Verifica-se que a propriedade de heap máximo é satisfeita no arranjo final: todo nó pai é maior ou igual aos seus filhos (por exemplo, `34 ≥ 21, 8`; `21 ≥ 13, 2`; `8 ≥ 1, 3`; `13 ≥ 5`).

### b) Justificativa da complexidade de `heapify`

A função `heapify` compara o nó `i` com seus dois filhos (`left(i)` e `right(i)`) em **tempo constante** — `O(1)` por chamada. Se houver troca, ela é chamada recursivamente sobre o filho para o qual o elemento "desceu".

No pior caso, o elemento precisa "descer" desde a raiz até uma folha, percorrendo um caminho cujo comprimento é igual à **altura da árvore binária** representada pelo heap.

Como o heap é uma árvore binária **completa** (todos os níveis cheios, exceto possivelmente o último), sua altura é:

$$ h = \lfloor \log_2 n \rfloor $$

onde $n$ é o número de elementos do heap.

Portanto, no pior caso, `heapify` realiza um número de operações proporcional à altura da árvore, resultando em complexidade $O(\log n)$ — cota que também é justa no pior caso, podendo ser expressa como $\Theta(\log n)$.