
|          |            |             |                      |         |
| -------- | ---------- | ----------- | -------------------- | ------- |
| X        | Sequencial | Binária     | Árvore Binária Busca | Hashing |
| Consulta | $O(n)$     | $O(log\:n)$ | $O(log\:n)^*$        |         |
| Inserção | $O(1)$     | $O(n)$      | $O(log\:n)^*$        |         |
| Remoção  | $O(1)$     | $O(n)$      | $O(log\:n)^*$        |         |

Árvore depende da ordem das entradas.

$*$﻿Apenas se a árvore estiver balanceada

Remoção:

- Maior da subárvore da esquerda
- Menor da subárvore da direita

## Hashing

Função que determina o índice a partir da chave passada

Queremos evitar colisão de hash, duas chaves com elementos iguais

$f(k) = f(q)$