## Notas
- Função PollardRho é muito mais rápida em fatorar primos, mas não é utilizada nos outros casos
	- a sua função modular_pow é o binpow, que deve ser implementado de alguma forma, ainda pode ser acelerado [CpAlgorithms](https://cp-algorithms.com/algebra/binary-exp.html#effective-computation-of-large-exponents-modulo-a-number)
	- se a lista de repetição é necessária, ordernar e iterar pelos fatores é mais fácil

- Input inicial poderia já formatar o número como mpz
- Passar o código para .py, receber entradas como `python3 script.py < entrada.txt`
- Modularização seria interessante, facilita leitura do código fonte para correção

- A contagem de testes de Miller está errada (eu acho)
- Não se quer contar o número de chamadas do Miller-Rabin, e sim a quantia de testes de Miller (quantos primos foram testados)

## Artigos Úteis do CPAlgorithms

Miller-Rabin e Versão Determinística: [Testes Primalidade](https://cp-algorithms.com/algebra/primality_tests.html#miller-rabin-primality-test)
$a^k\mod p$: [Binary Exponentiation](https://cp-algorithms.com/algebra/binary-exp.html#effective-computation-of-large-exponents-modulo-a-number)
Pollard $\rho$: [Fatoração](https://cp-algorithms.com/algebra/factorization.html#brents-algorithm)
Baby-Steps Giant-Steps: [Log Discreto](https://cp-algorithms.com/algebra/discrete-log.html)
