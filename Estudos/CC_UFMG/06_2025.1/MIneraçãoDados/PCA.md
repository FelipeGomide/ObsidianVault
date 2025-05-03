Tentar capturar as dimensões que melhor representam os dados.

A idéia é representar o mesmo hiperplano original com menos dimensões, sem perda significativa dos dados.


Objetivo: Encontrar base que maximize a variância dos dados. (consequentemente minimiza o erro quadrado dos dados)

OBS: O PCA parte do pressuposto de que não existem muitos outliers (caso hajam: variância alta, mas o resto dos dados é condensado)

Bases de vetores ortonormais.

Cada nova base, novo $\lambda$, a soma dos valores dos lambda é a variância total da projeção.
Quantos mais lambdas, mais variância e menos erro, logo, é possível explicar melhor os dados.
