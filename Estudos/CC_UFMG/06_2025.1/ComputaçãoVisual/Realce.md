Técnicas para acentuar ou melhorar a aparência de imagens.

## Transformação Escala de Cinza

Realizar transformações no histograma da imagem, facilitar a percepção da imagem.

Intervalo de contraste: 
Diferença de intensidade máximo e mínimo que f(x,y) pode assumir
Quando o intervalo não é todo ocupado, pode-se ampliar o intervalo de contraste para $[0,255]$.

## Equalização de Histograma

Modificar o histograma tal que o histograma da imagem resultado se aproxime de uma distribuição uniforme.

Calcular distribuição acumulada de probabilidade e utilizar probabilidade.
	É basicamente projetar no eixo Y de maneira mais uniforme

Percentual do cumulativo se torna valor do novo tom de cinza.
	Quantizar percentual $(0,1)$ em tom de cinza $(0,255)$. 

Aumentar a distribuição de tons de cinza: melhora o constraste da imagem.


Equalização apresentava valores "estourados", quantizar num intervalo $(25, 255)$ é saída?


## Pontilhado Ordenado

Transforma 1 pixel em 9, coloca pixels totalmente pretos ou brancos conforme valor em relação a 255.
Diminui pixel de 8 bits para 1, mas aumenta quantidade de pixels por 9. O ganho de entropia não resulta em compressão pelo aumento de resolução.
## Pontilhado com Difusão de Erro

Pixel é alterado para 0 ou 1 (mais próximo) e o erro é difundido para os 5 pixels próximos seguintes.
Divide o erro por 16 e distribui nas proporções devidas.


Prova vai até aqui. Filtragem não consta na primeira prova
