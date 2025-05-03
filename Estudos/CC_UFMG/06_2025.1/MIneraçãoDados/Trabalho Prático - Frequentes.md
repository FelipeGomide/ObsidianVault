# Parte 2
Usar LLM para auxiliar na tarefa.
Obter sugestões e resolver dúvidas - Seleção de Variáveis e Aplicação de Algoritmos

Criticar a sua eficácia, precisão e outras dimensões pertinentes.

### Jupyter Notebook:
1. Business Understanding:
- Objetivo do Dataset:
	Acidentes de trânsito são responsáveis por muitas mortes pipipi popopo, saúde pública, economia etc. (Isso tem no arquivo do projeto)
- Origem dos Dados:
	Paper linkado apresenta informações sobre a coleta dos dados, Dados de APIs públicas de trânsitos nos anos de 2016 a 2023, nos Estados Unidos, em principal, na Califórnia. (explicar isso melhor)
- Características do Dataset:
	O dataset apresenta informações quanto a acidentes de trânsito, apresenta variáveis como localização, condições climáticas no momento do acidente, sinalização de trânsito no local e severidade do acidente, a partir do quanto o acontecimento influenciou negativamente no tráfico de veículos na via.
- Relação com o Problema de Negócio:
	A partir dos dados presentes no dataset, é possível encontrar quais fatores combinados são os maiores responsáveis por acidentes. Assim, seria possível traçar planos de políticas públicas de forma a minimizar a quantidade ou o impacto dos acidentes.

2. Data Understanding:
- Exploração Inicial:
	TODO: Analisar distribuição de valores, estatísticas descritivas, VALORES NULOS
- Análise Visual:
	Gerar gráficos e visualizações para compreender os dados.

Data Preparation
- Limpeza de Dados:
	Simples, a base já é bem tratada, no máximo remover instâncias com valores nulos.
	O único problema é o grande volume de dados (7 milhões de instâncias).
	Podemos usar a versão de apenas 500k disponibilizada no Kaggle. Escolher as colunas que vamos usar, remover nulos e depois verificar o tamanho. Se ainda estiver muito grande, podemos restringir em relação ao Estado (maioria dos dados são de São Francisco) ou ano da informação.
- Transformação de Dados:
	Normalização, Discretização ou outras transformações (one-hot encoding?, categorização de dados numéricos para utilizar nos algoritmos)
- Seleção de Features:
	Precisamos da análise exploratória para escolher quais fatores utilizar, mas severity é necessário, é o que desejamos prever.
	Acho que buscamos por itemsets com todas os fatores escolhidos, menos severity, depois usamos regras de associação com os grupos formados para prever severity.

3. Modeling
	Diversos algoritmos, preciso usar um entre: {Apriot, Eclat, FP-Growth}
	(Posso pedir pro LLM uma implementação nessa fase 2 e depois utilizar uma biblioteca própria na fase 3)
	E também Association Rules a partir dos frequentes encontrados com um dos algoritmos anteriores.

	No primeiro passo, itens de suporte relativo alto indicam condições que geram muitos acidentes.
	No segundo, quero usar Association Rules para prever acidentes de Severity 4

4. Evaluation
- Análise de Resultados:
	Discutir os padrões encontrados e sua relevância para o problema.
- Avaliação dos Algoritmos:
	Criticar o desempenho dos algoritmos em eficiência e precisão.
- Considerações Finais:
	Reflexão sobre desafios enfrentados, o que funcionou e o que pode ser melhorado.