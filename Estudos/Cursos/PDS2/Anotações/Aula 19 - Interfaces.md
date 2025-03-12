Modelando diagramas funções

Acima: dados

Abaixo: funções

+: public

-: private

```Mermaid
classDiagram
  class Exemplo{
  +int idade
  -string nome
  +get_nome()
  -get_idade()
}
```

  

Interfaces/classes abstratas: solução para problemas com herança

Método:

virtual void exibir() = 0;

  

Toda classe com método abstrato (igual a 0) indica uma interface, uma classe que não pode ser criada. Todas as classes que a herdam são obrigadas a implementá-la.