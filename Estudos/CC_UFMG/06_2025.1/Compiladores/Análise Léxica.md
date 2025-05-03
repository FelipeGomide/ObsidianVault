Particionar todo o texto (incluindo caracteres especiais) em substrings ou Tokens.

## Tokens
São uma categoria sintática.
Identificador, Literal, Palavra reservada.

Correspondem a conjuntos de strings.
- Identificadores: strings com letras e algarismos, iniciado de letra.
- Literais:
	- Inteiros: string não vazia de algarismos, pode ser iniciada de `+` ou `-`
	- Float: `-6.02E-23`
	- string
	- booleanos
	- outros
- Palavras reservadas: "while", "if", "begin"
- Outros (operadores, pontuação, escopo, separadores, indexadores)

A ideia é conseguir classificar os substrings de acordo com o papel na sentença.
Entrega um array de tokens para o analisador sintático.

### Construção de um Analisador Léxico:
- Definir conjunto finito de tokens
	Alguns tokens precisam ser acompanhados da substring que os identificou.
	Identificadores, literais...
	Retorno então uma lista de pares	<Token, Lexema>
	
- Descartar caracteres desinteressantes
		Fortran: separadores não são significativos, 
		motivados pela imprecisão do cartão perfurado.
		`DO 5 I = 1,25`
		Estrutura de loop
		`DO 5 I = 1.25`
		Variável DO5I passa a ter o valor real 1.25

- Look Ahead:
	Ler os caracteres da entrada, reconhecendo os tokens na medida que aparecem.

	PL/I, todos os comandos não são palavras reservadas.
	`IF ELSE THEN THEN = ELSE; ELSE ELSE = THEN`
	Em C++, sintaxe de stream e aninhamento de templates.

Como fazer:
Utilizamos linguagens regulares
- Simples, mas suficientes pro problema
- Fáceis de implementar eficientemente

### Expressões Regulares

Solução mais popular para identificar tokens.

Linguagens:
Subconjunto dentre todas as sequências formadas por um alfabeto.

Notação padrão para linguages regulares: expressões regulares.

Expressões Atômicas:
$\epsilon$, A, B, C

Expressões Compostas:
- União:
	$[\epsilon, A]$
	$\epsilon + A$
- Concatenação:
	$AB$
- Fechamento (Kleene):
	$A^* =$  ""$, A, AA, AAA, ...$
	$A^+ = A, AA, AAA...$


Na hora de ler, princípios de ordem de declaração e maximal munch.