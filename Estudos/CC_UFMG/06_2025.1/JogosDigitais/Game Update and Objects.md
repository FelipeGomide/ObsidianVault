Aula passada: [[Game Loop]]
3 funções: *input, update, draw*
### Update Game
Controla / implementa toda a lógica do jogo.

Em jogos pequenos, é possível implementar tudo em uma função.
Quando o projeto fica um pouco mais complexo, já se torna um problema.

Abstrair o jogo como uma lista/array de GameObjects.
A função update do jogo percorre o array chamando o update, dos objetos, delegando a eles a obrigação de se atualizar.

Problema clássico: acoplamento de objetos

Adicionar e remover objetos da lista de GameObjects pode ser problemático.

Listas auxiliares de objetos pendentes a serem adicionados e objetos inativos. 

## Game Objects

Difíceis de representar por classes, muitos comportamentos distintos.

### Hierarquia de classes: 

Dificuldades: muito mutável, difícil de controlar, possíveis heranças múltiplas.

### Modelo de componentes: "Prefira composição à herança".

Cada *GameObject* possui uma lista de componentes (classes), que seja possível de plugar ou combinar de várias formas distintas.

Objetos são simples, e é possível adicionar componentes a ele.
Componentes possuem uma hierarquia de classes mais rasa.

*Problema clássico*: componentes são desacoplados, mas podem utilizar objetos em outros componentes.
- Realizar buscas lineares

Exs: RigidBody (dimensão e posição), Collider (Colisão), Draw (renderiação, sprites), Update (movimentação), Physics.

### Abordagem Híbrida:
