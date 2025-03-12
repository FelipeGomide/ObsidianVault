- Diversos contêineres com funções semelhantes, size, capacity, begin, end.

```Mermaid
classDiagram
direction TB
  class Container{
  +int size()=0;
  +<?> begin()=0;
  +<?> end()=0;
  +bool empty()=0;
}
 class sequential{
 +void push_back()=0;
}
 class set{
 +void insert()
}
Container <|-- sequential
Container <|-- set
sequential <|-- list
sequential <|-- vector
```

  

  

```Mermaid
classDiagram
  direction LR
  class Mensagem{
  +void exibir virtual=0;
  
}
  class Texto{
 
}

  class Img{
 
}
  class TextImg{
 
}

Mensagem <|-- Img

TextImg *-- Texto
Mensagem <|-- Texto
Mensagem <|-- TextImg

TextImg *-- Img
```