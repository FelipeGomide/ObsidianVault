```cpp
class Vector2 {
	float x,
	float y
}
```

Vetores 4D usados em jogos 3D para combinar transformações (rotação e translação).

### Operações:

- Soma: emenda um na ponta do outro
- Subtração: distância dos pontos
	(Não é comutativa, a direção apontada é oposta)
- Multiplicação por escalar: aumenta a intensidade/comprimento
	(se for negativa inverte a direção)
- Produto escalar:
	$\vec a * \vec b = a_x * b_x + a_y * b_y$
	Se $\hat a$ for unitário, $\hat a * \vec b$ é o comprimento da projeção de $\vec b$ em $\hat a$.
	Se dois vetores são perpendiculates, o produto é 0.
	Se dois unitários são paralelos 1, ou -1 (direções opostas).
- Norma (comprimento) e normalização.
- Produto Vetorial:
	Só é definido no 3D.
	$\vec a \times \vec b$ é o vetor normal ao plano desses dois vetores
### Inverter em relação a uma normal
Vetor $\vec v$ e normal da superfície $\hat n$
$\vec v' = \vec v + 2 \hat n (- \vec v * \hat n)$

