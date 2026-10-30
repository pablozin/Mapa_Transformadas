---
tags: [laplace, inversa, polos_complexos, nivel_medio]
origem: "Lathi Prob. 4.1-3b"
---
### Problema 4.1-3 (b)
Determine a transformada inversa de Laplace unilateral de:

$$X(s) = \frac{3s + 5}{s^2 + 4s + 13}$$

> [!tip]- Dica de Resolução
> As raízes são complexas ($-2 \pm j3$). Em vez de trabalhar com números imaginários, complete o quadrado no denominador: $(s+2)^2 + 3^2$, e ajuste o numerador para casar com as fórmulas de $\cos(3t)$ e $\text{sen}(3t)$ amortecidos por $e^{-2t}$.

> [!success]- Resolução Passo a Passo
> Completando o quadrado no denominador:
> 
> $$s^2 + 4s + 13 = (s + 2)^2 + 9 = (s + 2)^2 + 3^2$$
> 
> Reescrevendo o numerador em função do termo $(s + 2)$:
> 
> $$3s + 5 = 3(s + 2) - 6 + 5 = 3(s + 2) - 1$$
> 
> Ajustando o termo constante para isolar a frequência $\omega_0 = 3$:
> 
> $$3s + 5 = 3(s + 2) - \frac{1}{3}(3)$$
> 
> Separando a fração em duas partes correspondentes à tabela:
> 
> $$X(s) = 3 \frac{s + 2}{(s + 2)^2 + 3^2} - \frac{1}{3} \frac{3}{(s + 2)^2 + 3^2}$$
> 
> Aplicando a inversão direta (pares 9a e 9b):
> 
> $$x(t) = \left[ 3e^{-2t}\cos(3t) - \frac{1}{3}e^{-2t}\text{sen}(3t) \right] u(t)$$