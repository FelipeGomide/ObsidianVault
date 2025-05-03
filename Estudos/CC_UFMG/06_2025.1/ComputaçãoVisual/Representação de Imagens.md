Matriz bidimensional (cada elemento é um pixel).
Não se adapta aos dados, gera redundância.

Podem ser representadas em múltiplas resoluções, como uma pirâmide.
$8\times8,\space 4\times4,\space 2\times2,\space 1\times1$

(Versões menores podem ser mais fáceis de encontrar faces, por terem menos conteúdo)

[[Extração de Características]] (Módulo 2) Transformar imagem num vetor de características
- Imagem vira um ponto num espaço vetorial de características.
- Imagens próximas no espaço são similares.

### Imagens Multibands
O pixel é associado ao valor vetorial.
$f(x,y) = (l_1, l_2, ..., L_n)$ onde $L_{min} \leq L_i \leq L_{max}$.

Cada L pode representar grandezas distintas:
- Luminância: brilho
- Matiz: comprimento de onda dominante
- Saturação: pureza do matiz

Ou três cores primárias RGB (Red, Green, Blue) com 1 byte por banda/pixel.

### Ruído em Imagens

Degradação durante aquisão, transmissão ou processamento da imagem.
- Variável aleatória, função de densidade de probabilidade $p(z)$.

Ruído Impulsivo: ocorrência aleatória de pixels com valores de luminosidade bem distintos.

Ruído Gaussiano: ocorrência de pixels de intensidade que variam conforme a distribuição Gaussiana.
Remoção de ruído envolve mudar a imagem para o domínio de frequências e depois operar com esses novos dados.

### Entropia
Quantidade de informação transferida por um canal.
Quantidade de informação necessária para codificar uma imagem.

Distribuição de prob de níveis de intensidade de pixels:
$p_i = \dfrac{n_i}{n}$

Pode ser usada para diminuir a quantia de bits para representar a imagem.
Tabela de conversão da medida anterior para a nova.

*Entropia de uma imagem :

Medida positiva, quando log na base 2, unidade são bits
(quantos são necessários para representar a imagem)

Menor valor é 0 (todos pixels de mesma intensidade).
Máxima entropia quando a distribuição é uniforme.

Localização espacial não importa, apenas o histograma.

### Métricas de Qualidade

- Erro máximo: maior diferença absoluta entre cada ponto
(pouco representativo)

- Erro médio absoluto: média da soma da diferença absoluta de cada ponto
(não penaliza tanto erros em poucas áreas)

- Erro médio quadrático: média da soma do quadrado das diferenças de cada ponto
(melhor métrica)
