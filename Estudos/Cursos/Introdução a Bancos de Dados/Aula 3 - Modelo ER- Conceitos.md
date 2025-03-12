# Modelo entidade-relacionamento

Esquema em diagrama: remove ambiguidades nos esquemas

  

## Entidades

---

Instância de interesse em uma aplicação

- Descrita por seus atributos:
    - ID: 001
    - Nome: João

  

### Tipo de entidade: (Quadrados)

Descreve o modelo para um conjunto de entidades que compartilham atributos

  

### Tipos de atributo: (círculos)

- Simples: admite valores escalares
- Composto: admite tuplas como valores

  

- Monovalurado: admite somente um valor
- Multivalorado: admite vários valores (borda dupla)

  

- Armazenado: deve persistir no banco
- Derivado: deve ser computado sob demanda (pontilhado)

  

A modelagem conceitual não impõe uma escolha, apenas indica possibilidades.

Decisões geralmente ponderam entre custo e eficiência.

  

Chave de um tipo de entidade:

- Possui valor distinto para cada entidade.
- Denotada pelo sublinhado.
- Pode ser formada por vários atributos (a tupla deve ser única, podem haver elementos repetidos)

  

## Relacionamentos

---

Associação entre duas ou mais entidades distintas, com semântica definida.

e¹ : empregado João Silva

d³: departamento financeiro

e¹↔d³

  

### Tipos de relacionamento: (Losangos)

Define um conjunto de relacionamento entre instâncias de um ou mais tipos de entidade

  

Atributos em tipos de relacionamentos.

Par de instâncias que participam são implicitamente uma chave, podem ser adicionadas novas chaves.

  

### Restrições sobre relacionamentos

Dois tipos: participação e cardinalidade

Participação: mínimo de instâncias que uma instância deve associar

- Barra dupla, total, necessidade de 1
- Barra simpes, parcial, mínimo 0

Notação “look here”, mesmo lado

  

Cardinalidade: máximo de instâncias de um relacionamento que uma entidade pode se associar

Denotada pelos numerozinhos.

Notação “look across” pelo lado oposto.

  

---

Entidade fraca: não possui chava própria (borda dupla)

Chave parcial: insuficiente para identificação (sublinhado tracejado)

  

Relacionamento identificador (borda dupla)

Liga uma entidade forte e uma fraca

  

Combinação da chave parcial e da chave forte identificam a entidade fraca

---

## Aridade de Relacionamentos

Relacionamento unário: envolvem instâncias de um único tipo.

- Instâncias atuam com certo papel (escrita na linha)

  

Entidades associativas: relacionamento que atua como entidade.

a : (e1, p2)

x :((e1,p2),f7)