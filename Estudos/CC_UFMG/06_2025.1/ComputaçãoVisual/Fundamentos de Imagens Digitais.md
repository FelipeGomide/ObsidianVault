- Livro: Análise de Imagens Digitais: Princípios, Algoritmos e Aplicações
	- Bibliteca online: Base de Dados "Cengage Learning"

## Modelos de Imagens
Função de intensidade luminosa f(x,y) fornece a intensidade da luz em um ponto.
(0,0) parte do ponto superior esquerdo.

Dois pontos de influência: intensidade da luz e características da superfície que a reflete.

Produto entre quantidade de luz incidente e reflectância dos objetos.
$f(x,y) = i(x,y) \space r(x,y)$

Iluminância em lúmen/m², reflectância em porcentagem.
$0 < r(x,y) < 1$
$0<i(x,y)< infinito$

Iluminância cresce infinitamente, como resolver?
Definir um teto, e utilizar uma escala logarítmica.
Motivo: Olho humano é bom em detectar formas em baixa luminosidade.

Diferenças são boas, ajudam a detectar formas.
Equalização de histograma ajuda a uniformizar tons de cinza.

### Digitalização em dois passos: amostragem e quantização
*Amostragem:* discretizo o domínio da definição de imagem em uma matriz MxN
- Tradeoff: 
		poucos pixels = perda de informação
		muitos pixels = redundância

*Quantização*: Um número inteiro L de níveis de cinza para cada ponto da imagem

Frequência espacial de amostragen
$F_a = \dfrac{1}{\Delta x}$ 

Teorema de amostragem de Nyquist-Shannon
$\Delta x \leq \dfrac{1}{2B}$
Para se obter uma amostragem suficientemente boa

$f(x,y)$ tem banda delimitada no domínio da frequência $[-B, B]$.

### Resolução espacial
Densidade de pixels da imagem, quanto menor o intervalo de amostragem $\Delta x$, maior densidade e maior resolução espacial.

Densidade: qual a dimensão no mundo real que cada pixel representa, quantos cm² por pixel.

### Profundidade da imagem

Número de tons de cinza $L$.
$L = 2^b$
b é a profundidade da imagem

Tamanho da imagem: número de pixels * profundidade.

