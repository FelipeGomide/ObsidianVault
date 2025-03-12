Relação entre classes do qual uma classe herda características de outra classe.

```C++
Veículo {
    string cor;
    unsigned int placa;
}
```

- Moto
- Pool
- Uber

Todas formas de transporte utilizam da classe veículo.

```C++
Class UberMoto : public Uber {
public:
	UberMoto(
		string _cor;
		unsigned int _placa;
	);
};
```

  

Uber moto reutiliza tudo do public de Veículo.

  

**virtual** unsigned int get_num_passageiros();

Método pode ser alterado por herdeiros.

  

unsigned int get_num_passageiros() **override**;

Reescreve um método existente.

  

Forma mais rápida de fazer construtores:

Uber::Uber(cor, placa) : _cor(cor), _placa(placa){}

  

Processo para o herdeiro:

UberMoto::UberMoto(cor, placa, bau) : Uber(cor, placa), _bau(bau) {}

Dessa forma, os dados já são inseridos no mesmo momento da alocação do objeto na memória.

  

  

Classes:

pais/filhas

Superclasses/subclasses

  

Pessoa p = Pessoa(idade, nome);

Pessoa p(idade, nome);