Gerenciamento de memória, localidade de espaço e tempo.

  

## Modelos Agregados

“Agregados são coleções de itens relacionados que desejamos que sejam tratados como uma unidade”

- Facilitam o trabalho em clusters
    - Minimiza o número de nodos para informações
- Auxilia em operações de transação

### Agregados opacos:

Agregado é um blob

Guarda o que quiser com uma chave

Só poder fazer query pela chave

### Agregados transparentes:

Agregado possui estrutura: json, xml

Busca por valor ou chave

  

## Key-Value API

Operações:

- get(key)
- set(key, value, [ttl]) time to leave
- del(key)

Data types:

- blob
- list, set, hash of blob

  

## Column-Family

Appends eficientes, bom para escritas constantes

Tamanho inconstante, atributos diferentes para diferentes entidades

  

## Column family API

Operações:

- get(cfamily, row, [column])
- set(cfamily, row, column, value)
- del(cfamily, row, [column])

Ou

- CQL: simples SQL flavour

SQL da Cassandra