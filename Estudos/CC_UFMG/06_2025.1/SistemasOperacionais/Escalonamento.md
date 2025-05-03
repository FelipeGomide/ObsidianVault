Motivações:
- Medida para controlar compartilhamento de recursos
- Utilização simultânea de vários usuário (mainframes e nuvem)
- Maximizar uso da CPU (Processos bloqueados não param CPU


Escalonamento ocorre quando forçam a troca do processo a ser executado:
- Eventos de interrupção (bloqueiam o processo)
- Erros
- I/O
- Comunicação e sincronização


Diversas políticas de escalonamento, diferentes objetivos.

### Métricas:
*throughput*: # jobs por segundo
*turnaround*: tempo entre submissão e conclusão
*tempo de resposta*: tempo entre submissão e início da execução (minimizar em programas interativos)
*eficiência*: minimizar o overhead
*prioridade*


Preempção
Política não-preemptiva: o processo nunca é interrompido, apenas termina ou é bloqueado
Política preemptiva: processo pode ser interrompido antes de terminar
	processos tem um quantum de tempo de execução.


## Políticas de Escalonamento
### FIFO
First-in First-out
Não-preemptivo
Simples, fácil de implementar
### SJF
Shortest job first
Menor tempo de espera de todas.
Difícil de calcular o tamanho do processo:
	estimar o tamanho do _burst_ a partir do tamanho do anterior
Cisne Negro: evento atípico fora do modelo/esperado

### Round Robin
Adotar um quantum de tempo. Ao esgotar é colocado de volta na fila.
Todos processos dividem igualmente o processamento.
Usado virtualmente por todos SOs
Tamanho do quantum:
- baixo: troca de contexto cara
- alto: tempo de resposta alto
Desvantagem: todo mundo roda um pouco até terminar um processo.

### Prioridades
Processos com prioridade maior rodam primeiro

Aloção das prioridades:
Estática: processos importantes primeiro
Dinâmica: processos perto do prazo primeiro, depende do contexto

### Filas múltiplas
Várias filas, cada uma com uma política distinta.
Política de escalonamento entre filas.
Permite maior sofisticação.
Difícil de prever o comportamento.

### Filas múltiplas com realimentação
Processos podem mudar de filas.
Políticas de promoção e rebaixamento.

##### Exemplo: 4.3 BSD Unix
Entre filas: prioridade
Dentro da fila: round robin

Usou todo o quantum? --
Está esperando muito? ++ (aging)

Processos interativos rodam mais rápido, processos com muita CPU rodam depois.

##### Exemplo: BrainF* scheduler
Fila única, processos tem niceness

##### Exemplo - CFS
Completely fair scheduler
Cada processo tem uma fatia igual de um processo

#### Avaliação analítica
Uso de métricas
Teoria das filas
Simulação
Verificação automática