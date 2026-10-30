---
tags: [laplace, inversa, fracoes_parciais, nivel_facil]
origem: "Lathi Prob. 4.1-3a"
---
### Problema 4.1-3 (a)
Determine a transformada inversa de Laplace (unilateral) de:

$$X(s) = \frac{2s + 5}{s^2 + 5s + 6}$$

> [!tip]- Dica de Resolução
> O denominador fatora em $(s+2)(s+3)$. Como os polos são reais e simples, monte as frações parciais e calcule os resíduos tampando o polo avaliado (Heaviside).

> [!success]- Resolução Passo a Passo
> Fatorando o polinômio do denominador:
> 
> $$X(s) = \frac{2s + 5}{(s + 2)(s + 3)} = \frac{k_1}{s + 2} + \frac{k_2}{s + 3}$$
> 
> Calculando os resíduos pelo método de Heaviside:
> 
> $$k_1 = \left. \frac{2s + 5}{s + 3} \right|_{s = -2} = \frac{2(-2) + 5}{-2 + 3} = \frac{1}{1} = 1$$
> 
> $$k_2 = \left. \frac{2s + 5}{s + 2} \right|_{s = -3} = \frac{2(-3) + 5}{-3 + 2} = \frac{-1}{-1} = 1$$
> 
> Reescrevendo $X(s)$ com os coeficientes encontrados:
> 
> $$X(s) = \frac{1}{s + 2} + \frac{1}{s + 3}$$
> 
> Aplicando a transformada inversa imediata da tabela (par 5: $\frac{1}{s - \lambda} \iff e^{\lambda t}u(t)$):
> 
> $$x(t) = \left( e^{-2t} + e^{-3t} \right) u(t)$$