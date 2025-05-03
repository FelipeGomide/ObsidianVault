### Suporte
Quantidade de transações que contém ambos X e Y.
$sup(X \rightarrow Y)  = sup(XY) = |t(XY)|$

O suporte adequado depende de $|D|$, tamanho do banco de dados.

### Suporte relativo
Probabilidade de ocorrer, frequência relativa.

$rsup(XY) = \dfrac{sup(XY)}{|D|}$

Probabilidade no conceito frequentista:
	Seja $n$ vezes realizado um experimento. Então a prob de A é 
		$P(A) = \lim \dfrac{\#A}{n}$

### Confiança
Probabilidade condicional que uma transação contém o consequente Y dado que contém X.

$P(XY) = \dfrac{\# XY}{|D|}$

$P(Y|X) = \dfrac{\#XY}{\#X}$


Confiança deve ser avalianda considerando o suporte das regras.

Se $P(BC) = 0.67$, a regra $E \rightarrow BC$ com $0.60$ de confiança, tem efeito deletério em BC.

### Lift

$lift(X \rightarrow Y) = \dfrac{P(XY)}{P(X)\times P(Y)}$

Se A e B são independentes, $P(AB) = P(A) \times P(B)$.

$P(A|B) = \dfrac {P(A)\times P(B)}{P(B)} = P(A)$

Lift alto: regras atrativas, frequência muito grande deles juntos se separados.
Lift pequeno <1: repulsividade das duas regras.

Escala não é linear antes e depois de 1. escala relativa
### Leverage

Mede diferença entre o observado e o esperado dado que X e Y são independentes.

$leverage(X \rightarrow Y) = P(XY) - P(X) \times P(Y)$

É preciso avaliar se existe também uma frequência mínima do evento: suporte relativo.

### Coeficiente de Jaccard
Mede a similaridade de dois conjuntos.

$0 \leq \dfrac{Interseção}{União} \leq 1$

$\dfrac{P(XY)}{P(X)+P(Y)-P(XY)}$


### Avaliação Conjunta
*Lift e Leverage*
Lift e Leverage devem ser avaliados juntos, o mesmo lift pode se referir a leverages bastante distintas.
Leverage (distância absoluta) grande é mais significativo em lifts iguais.

*Lift e Confiança*
Quanto maior a confiança, maior a representatividade da regra quando existe algum Lift.

*Lift e Jaccard*
Relação similar, mas no intervalo $[0,1]$ 

Métricas simétricas: não enviesar em apenas um dos sentidos.
Métricas assimétricas: cuidado com a direção da métrica.

### Tabela de Contingência, matriz de confusão

### Convicção
Mede o erro esperado da regra, quão frequentemente X ocorre onde Y não ocorre.

$conv(X \rightarrow Y) = \dfrac{P(X) \times P(\neg Y)}{P(X \neg Y)} = \dfrac{1}{lift(X \longrightarrow \neg Y)}$

### Odds e Oddsratio



## Depois de encontrar uma regra aparentemente boa

Checar Lift Médio e Suporte Relativo Médio de todas combinações do conjunto da regra, em ambos sentidos.

Conferir se as métricas da regra encontrada em específico diverge das médias.

rsup possui certa sensibilidade, depende do tamanho e variabilidade do banco de dados.