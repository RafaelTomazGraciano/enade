## Questão 20

### Texto

Observe o código abaixo escrito na linguagem C.

```c
1   #include <stdio.h>
2   #define TAM 10
3   int funcao1(int vetor[], int v){
4       int i;
5       for (i = 0; i < TAM; i++){
6           if (vetor[i] == v)
7               return i;
8       }
9       return -1;
10  }
11  int funcao2(int vetor[], int v, int i, int f){
12      int m = (i + f) / 2;
13      if (v == vetor[m])
14          return m;
15      if (i >= f)
16          return -1;
17      if (v > vetor[m])
18          return funcao2(vetor, v, m+1, f);
19      else
20          return funcao2(vetor, v, i, m-1);
21  }
22  int main(){
23      int vetor[TAM] = {1, 3, 5, 7, 9, 11, 13, 15, 17, 19};
24      printf("%d - %d", funcao1(vetor, 15), funcao2(vetor, 15, 0, TAM-1));
25      return 0;
26  }
```

---
## Enunciado

A respeito das funções implementadas, avalie as afirmações a seguir.

> **I.** O resultado da impressão na linha 24 é: 7 - 7.

> **II.** A função `funcao1`, no pior caso, é uma estratégia mais rápida do que a `funcao2`.

> **III.** A função `funcao2` implementa uma estratégia iterativa na concepção do algoritmo.

É correto o que se afirma em

- **A)** I, apenas.
- **B)** III, apenas.
- **C)** I e II, apenas.
- **D)** II e III, apenas.
- **E)** I, II e III.

---
## Resposta

> **Letra A**

---
## Explicação

A `funcao1` percorre o vetor do início ao fim comparando cada elemento com o valor buscado. Essa é a **busca sequencial** (ou busca linear). A `funcao2` divide o vetor ao meio a cada chamada e decide em qual metade continuar a busca. Essa é a **busca binária**, implementada de forma recursiva.

**Afirmação I:**

O vetor é `{1, 3, 5, 7, 9, 11, 13, 15, 17, 19}` e o valor buscado é 15.

Na `funcao1`, o laço percorre o vetor do índice 0 ao 9. O valor 15 está na posição de índice 7. Portanto, a função retorna **7**.

Na `funcao2`, com a busca binária:

- Primeira chamada: i=0, f=9, m=4 → vetor[4]=9, como 15 > 9, busca na metade direita
- Segunda chamada: i=5, f=9, m=7 → vetor[7]=15, valor encontrado, retorna **7**

O resultado impresso é `7 - 7`. A afirmação I é **verdadeira**.

**Afirmação II:**

No pior caso, a `funcao1` (busca sequencial) percorre todos os N elementos do vetor, tendo complexidade O(N). A `funcao2` (busca binária) tem complexidade O(log N) no pior caso, ou seja, é muito mais rápida. Portanto, afirmar que a `funcao1` é mais rápida no pior caso é **falso**.

**Afirmação III:**

A `funcao2` chama a si mesma (linhas 18 e 20), o que caracteriza uma implementação **recursiva**, não iterativa. Uma implementação iterativa usaria um laço como `for` ou `while`. A afirmação III é **falsa**.

Como apenas a afirmação I é verdadeira, a resposta correta é a letra A.
