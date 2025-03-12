### Apêndice

---

Awesome cpp - Listas de Bibliotecas por tema

github.com/CrowCpp/crow

Cocos2D

Sqlite

Obs: Tomar preferência por single-header

Upcast: sobe na herança, pode ser feito.

Downcast: desce na herança, não é possível pois faltam elementos.

Dynamic Cast: apenas ponteiros

Se não for possível, (cast incorreto) ponteiro nulo

---

## Polimorfismo:

---

Polimorfismo: Método possui um funcionamento diferente dependendo do objeto que o chama.

```C++
moto.num_passageiros() // retorna 1
uber.num_passageiros() // retorna 4
```

```C++
UberMoto *normal = \
dynamic_cast<UberMoto*>(moto);
```

  

Referência em tipo:

Heranças são truncadas ao entrarem na função que recebe a superclasse

  

Referência em memória &:

Se refere ao endereço da classe, sem perder a informação das heranças. Mas sem acesso a elas

  

Herança:

Subir: mais geral

Descer: mais especializado

  

Virtual Override:

Late binding → ocorre em tempo de execução