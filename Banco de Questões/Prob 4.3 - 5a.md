---
tags: [laplace, funcao_transferencia, edo, nivel_facil]
origem: "Lathi Prob. 4.3-5a"
---
### Problema 4.3-5 (a)
Para o sistema descrito pela equação diferencial a seguir, determine a sua função de transferência $H(s)$:

$$\frac{d^2y}{dt^2} + 11\frac{dy}{dt} + 24y(t) = 5\frac{dx}{dt} + 3x(t)$$

> [!tip]- Dica de Resolução
> A função de transferência $H(s) = \frac{Y(s)}{X(s)}$ considera **todas as condições iniciais nulas**. Cada operador diferencial $\frac{d^n}{dt^n}$ vira simplesmente $s^n$.

> [!success]- Resolução Passo a Passo
> Aplicando a transformada de Laplace em ambos os lados, considerando condições iniciais nulas (sistema em repouso):
> 
> $$s^2 Y(s) + 11s Y(s) + 24 Y(s) = 5s X(s) + 3 X(s)$$
> 
> Colocando as transformadas $Y(s)$ e $X(s)$ em evidência:
> 
> $$(s^2 + 11s + 24) Y(s) = (5s + 3) X(s)$$
> 
> Isolando a razão entre a saída e a entrada para obter $H(s)$:
> 
> $$H(s) = \frac{Y(s)}{X(s)} = \frac{5s + 3}{s^2 + 11s + 24}$$
> 
> Fatorando o denominador para explicitar os polos:
> 
> $$H(s) = \frac{5s + 3}{(s + 3)(s + 8)}$$