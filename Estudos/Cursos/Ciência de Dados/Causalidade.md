 Base de dados/experimento:
 - Necessário grupo controle similar ao grupo da característica que se deseja estudar.
 - Grupos devem ser aleatórios e similares

Detectar viés/acaso:
- Teste de hipótese nula
	- Se um viés se confirmar, não se afirma a hipótese alternativa, apenas rejeitamos a nula

- Teste de permutação:
	- Quebra associação dos rótulos de forma randômica
	- Simula mundos aleatórios e calcula IC
	- Permutação com `shuffle`

- Bootstraping:
	- Não quebra associação de rótulos
	- Gera testes com reposição, simulando a geração de outro teste

- P-valor: chance de um valor mais extremo que o ocorrido
- Intervalo de Confiança: valores limites de um intervalo de uma % de significância
	- Autores sugerem 5% de significância

- Quando N é suficientemente grande, não é possível fazer teste de hipótese, qualquer dado tende a ser diferente da média.
	- N muito grande, dp muito pequeno

- Não é possível fazer IC Normal de outras medidas sem ser a média
	- Bootstrap ou permutação pode

