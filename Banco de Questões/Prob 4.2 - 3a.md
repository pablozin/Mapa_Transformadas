---
tags: [laplace, inversa, deslocamento_tempo, nivel_medio]
origem: "Lathi Prob. 4.2-3a"
---
### Problema 4.2-3 (a)
Determine a transformada inversa de Laplace de:

$$X(s) = \frac{2s + 5}{s^2 + 5s + 6} e^{-2s}$$

> [!tip]- Dica de Resolução
> O termo $e^{-2s}$ representa um atraso no tempo de $t_0 = 2$ segundos. Isole a fração racional, encontre sua inversa no tempo $x_1(t)$, e ao final troque cada $t$ por $(t - 2)$ com degrau $u(t - 2)$.

> [!success]- Resolução Passo a Passo
> Isolando a função racional sem o atraso:
> 
> $$X_1(s) = \frac{2s + 5}{s^2 + 5s + 6} = \frac{1}{s + 2} + \frac{1}{s + 3}$$
> 
> Invertendo $X_1(s)$ para o domínio do tempo:
> 
> $$x_1(t) = \left( e^{-2t} + e^{-3t} \right) u(t)$$
> 
> Usando a propriedade do deslocamento no tempo $\mathcal{L}^{-1}\{X_1(s)e^{-st_0}\} = x_1(t - t_0)u(t - t_0)$ com $t_0 = 2$:
> 
> $$x(t) = x_1(t - 2)u(t - 2)$$
> 
> Substituindo formalmente a variável $t$:
> 
> $$x(t) = \left[ e^{-2(t - 2)} + e^{-3(t - 2)} \right] u(t - 2)$$