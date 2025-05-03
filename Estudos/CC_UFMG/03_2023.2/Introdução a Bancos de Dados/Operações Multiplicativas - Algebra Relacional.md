Álgebra Relacional: operações com conjuntos

**Álgebra relacional**: operações com conjuntos

**Operações aditivas**: “básicas”, união, interseção e diferença.

  

# Operações Multiplicativas:

---

## Produto Cartesiano

Multiplica as tuplas de R com S

Notação: R x S

Características:

| R x S | = |R||S|

  

Esse produto cria tuplas espúrias, pois gera combinação exaustiva, todos com todos.

  

Seleção filtra as linhas por igualdade para eliminar tuplas espúrias. Comumente são feitas através da chave estrangeira.

  

## Junção (Join)

Combina tuplas que satisfazem uma condição lógica.

  

Notação:

R |><|[condição] S

$$

### Tipos de junção:

---

Junção simples.

**Equijunção:**

- Junção se dá por um teste de igualdade

**Junção natural:**

- Junção ocorre de forma implícita
- Teste de igualdade em atributos de mesmo nome
- Não necessariamente tem a mesma semântica (Prefixos solucionam problemas)
- Atributo de mesmo nome é unificado

  

## Autojunção:

Junção de uma tabela consigo mesma, gera pares de objetos da mesma tabela.

A forma natural retorna a mesma tabela.

Operador < ao invés de =/= resolve problemas de duplicidade.

  

### Junção externa(outer join):

---

Dada duas relações R e S qualquer, combina tuplas que satisfaçam uma condição lógica, e possivelmente tuplas que não a satisfazem.

Junção à esquerda, á direita e full outer

KaTeX parse error: Undefined control sequence: \leftouterjoin at position 1: \̲l̲e̲f̲t̲o̲u̲t̲e̲r̲j̲o̲i̲n̲  
̲\fullouterjoin

---

  

Externa à esquerda: tabela da direita pode conter nulos.

  

## Divisão:

$R \gets\pi_{EID,PID}Alocação \\$