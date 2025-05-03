Avaliar uma estatística baseada em uma variável categórica, geralmente sim ou não.

- Visualização dos dados, é comum adicionar um erro gaussiano para distanciar os pontos do scatterplot.
	- Borda branca, alpha baixo

- Curva logística: $y = \dfrac{1}{1+e^{-x}}$

- Pode-se pensar nela como: $y = \dfrac{1}{1+e^{\theta _1 x + \theta _0}}$

- Centrar os dados em x (subtrair a média)
	- Anula o valor de $\theta _0$
- Calcular a verossemelhança para $\theta _1$ (gradiente descendente)
- Entropia cruzada média = negativo da verossemelhança