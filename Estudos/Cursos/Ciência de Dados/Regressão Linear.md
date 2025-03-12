- Variância sumariza dispersão de uma coluna de dados
- Como proceder dados bidimensionais

Seaborn.pairplot() gera correlações entre estatísticas do dataset

Correlação entre rankings:
- Funciona independente do tipo de distribuição, quadrática, exponencial, quadrática
- Diferenças de unidade são perdidas, mantém-se apenas a ordem
- Correlação de Postos de Spearman

Paradoxo de Simpson:
- Correlações em pequenos grupos que em um grupo completo pode não se expressar ou se inverter
- Exemplo real: respostas no StackOverflow
	- Quanto mais respostas contínuas, melhor a resposta
	- Porém entre grupos que respondem o mesmo, a resposta piora



Mínimos Quadrados:
$\sum_{i=1}^n(y_i-\bar y_i)² = \sum_{i=1}^n(y_i-a -bx_i)²$ 

Se os dados são centralizados (subtraio a média de todos dados), gera-se uma função que passa pela origem, logo o a passa a ser descartado:

$\sum_{i=1}^n(y_i-bx_i)²$ 
Derivando por B: $\dfrac{dL}{dB}$
$b = \dfrac{\sum x_iy_i}{\sum x_i^2}$

$b = \dfrac{cov(x,y)}{var(x)}$



## Calculando a regressão:
- Bibliotecas statsmodels
- sm.add_constant(df) para adicionar uma constante 1
	- importante para calcular variável independente (intercepto)
- model = sm.OLS(endog=y, exog=x)
- fitted = model.fit()
- print(fitted.summary())