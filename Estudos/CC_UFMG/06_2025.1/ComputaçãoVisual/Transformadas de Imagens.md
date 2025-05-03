Transformadas alteram o domínio das imagens:
Domínio Espacial -> Domínio de Frequências

Podem ser feitas alterações no espaço de frequências e aplicar a transformada inversa para remover ruído de imagens.


SVD: Capturar variância dos dados

Fourier: Gera duas matrizes, é redundante
DCT: (Transformada discreta do cosseno)

Cap 3 do livro


Fourier: Decompor uma função em componente simples
- Decomposição em função de senos e cossenos
- Detectar frequências da função


Núcleo da Transformada:
Matriz $A$ de fórmula conhecida em DCT
(não precisa ser transmitida como Bases e AutoValores como na SVD)

Transformada é
$y = Ax^t$

$x' = [+|+|+|+|+|+]$
$x'' = [+|+|+|-|-|-]$

$y_1x' = 1$
$y_2x' = 0$

$y_1x'' = 0$
$y_2x'' = 1$

Cada linha de A representa uma frequência. Se o produto de X por ela é diferente de zero, existe a presença daquele padrão.

Dimensões de Frequências também podem ser utilizadas em classificadores de aprendizado de máquina.

Custo quadrático: Uma dimensão
Custo $O(n^4)$: 2D
Criar um vetor NxM e depois aplicar a Transformada

Não é ideal, custo explode, e captura valores globais, muitas frequências  distintas e muitos coeficientes a se guardar.
Quebrar a imagem em vários pedaços: frequências mais redundantes.

Fourier é invariante à translação, mas variante à rotação.
Espectro rotaciona junto com a imagem.
Fourier é preciso guardar coeficientes reais e complexos.
Muita redundância, ruim para compressão.