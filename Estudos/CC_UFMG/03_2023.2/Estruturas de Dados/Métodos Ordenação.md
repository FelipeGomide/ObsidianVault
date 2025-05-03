Métodos comparativos:

$\Omega (n*log(n))$

## Bubble sort

---

Compara elementos 2 a 2, mantém ou inverte a posição dos 2.

```C++
void bubble(item* v, int n){
  int i, j;
  for (i=0;i<n-1;i++){
    for (j=1 ; j<n-i ; j++){
      if (v[j].chave < v[j-1].chave) troca;
    }
  }
}
//Tal que n é o tamanho do array v
```

Estável: mantém a ordem de elementos de mesmo valor

  

$C(n) = \sum_{i=0}^{n-1}i$

((n-1)(n-2))/R

$C \in O(n^2)$

$T \in O(n^2)$

## Método Seleção

---

```C++
void selection(item* v, int n){
  int i, j, min;
  for (i=0; i<n-1; i++){
    min = i;
    for (j=i+1 ; j<n ; j++){
      if (v[j].chave < v[min].chave){
        min = j;
      }
    }
    Troca(v[i],v[min]
  }
}
//Tal que n é o tamanho do array v
```

Estabilidade: Não é estável

Vantajoso quanto a quantidade $n$﻿ de movimento de registro.

Bom para pequenos registros.

$C \in O(n^2)$

$T \in O(n)$

## Método Inserção

---

```C++
void insertion(item* v, int n){
  int i, j;
  item aux;
  for (i=1; i<n; i++){
    aux = v[i];
    j = i-1;
    while(j>=0 && aux.chave<v[j].chave){
      v[j+1]=v[j];
      j--;
    }
  v[j+1] = aux;
  }
}
//Tal que n é o tamanho do array v
```

É estável e adaptável

Melhor caso:

$C(n) \in O(n)$

Pior caso:

$C(n) \in O(n^2)$

Melhor caso:

$M(n) \in O(n)$

Pior caso:

$M(n) \in O(n^2)$

Posição -1 fantasma otimiza j≥0

## Merge Sort

---

Estabilidade: estável se ≤

Adaptável: Não, sempre realiza o mesmo número de operações, independente da ordem de entrada

Custo O(n log n)

Requer expaço extra proporcional a n

Se a implementação for melhor, memória extra = n log n

## Quick Sort

---

Rearranjo a partir de um pivô aleatório

Particionamento em duas partes:

- Direita: $chaves ≤ x$﻿
- Esquerda: $chaves ≥ x$﻿

Cursores **$i$**﻿ e $j$﻿ realizam n iterações até a partição.

Realiza o _**quicksort**_ das partições

- Estabilidade: não é estável
- Pior caso: pivô é o maior ou menor, partições 1 e n-1 O(n²)
- Melhor caso: pivô divide o vetor ao meio, $(1,386n*log(n) - 0,846 n)$﻿

Melhorias:

- Usar mediana de três para escolher o pivô
- Utilizar um algoritmo simples para partições pequenas
- Remover a recursão

  

## HeapSort

---

Algoritmo:

1. Seleciona o menor item do vetor
2. Troque-o com a última posição do vetor
3. Repita as operações com os n-1 itens restantes

Constroi: $n*log(n)$﻿

Ordena: $n*log(n)$﻿

Método instável

$O(n*log(n))$﻿

Bom para casos em que não são toleráveis casos desfavoráveis

Mais lento que o quicksort, porém mais constante, não têm pior caso

Não recomendado para arquivos com poucos registros

## Counting Sort

Efetivo $O(n+k)$﻿

n número de elementos e k valor do maior elemento

É necessário ter os limites dos valores bem definidos

Muita memória extra

  

  

## Bucket Sort

Separa os elementos em baldes de tamanho menor

Ordena cada um dos baldos usando os algoritmos tradicionais

n elementos e k buckets

Tempo $O(n²/k)$﻿

Espaço $O(n+k)$﻿

Vantagem: ordenação quasi-linear

Desvantagem: muita memória extra

## Radix Sort

Usa a representação binária das chaves para ordenação

Instruções bitwise são muito eficientes, se traduzem diretamente para o assembly

$O(n\:log(n))$