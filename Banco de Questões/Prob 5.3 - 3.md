---
tags: [transformada_z, equacoes_diferenca, condicoes_iniciais, transitoria_permanente, nivel_dificil]
origem: "Lathi Prob. 5.3-3"
---
### Problema 5.3-3
Resolva a seguinte equação de diferenças para $n \ge 0$:

$$2y[n + 2] - 3y[n + 1] + y[n] = 4x[n + 2] - 3x[n + 1]$$

Condições iniciais: $y[-1] = 0$, $y[-2] = 1$.  
Entrada: $x[n] = (4)^{-n} u[n] = (0,25)^n u[n]$.  
Determine as componentes **Transitória** ($y_{tr}[n]$) e de **Regime Permanente** ($y_{ss}[n]$).

> [!tip]- Dica de Resolução
> Converta o formato de avanço para a forma de atraso substituindo $n$ por $n - 2$. Em seguida, aplique as propriedades de atraso com as condições iniciais em $n = -1$ e $n = -2$.

> [!success]- Resolução Passo a Passo
> Reescrevendo a equação no operador de atraso (substituindo $n$ por $n - 2$):
> 
> $$2y[n] - 3y[n - 1] + y[n - 2] = 4x[n] - 3x[n - 1]$$
> 
> Aplicando a Transformada Z com as condições iniciais:
> 
> $$2Y[z] - 3[z^{-1}Y[z] + 0] + [z^{-2}Y[z] + 0 + 1] = 4X[z] - 3z^{-1}X[z]$$
> 
> $$(2 - 3z^{-1} + z^{-2})Y[z] + 1 = (4 - 3z^{-1})X[z]$$
> 
> Multiplicando toda a equação por $z^2$:
> 
> $$(2z^2 - 3z + 1)Y[z] = -z^2 + z(4z - 3)X[z]$$
> 
> Fatorando o polinômio característico:
> 
> $$2z^2 - 3z + 1 = 2(z - 1)(z - 0,5)$$
> 
> Substituindo $X[z] = \frac{z}{z - 0,25}$ e resolvendo as frações de $\frac{Y[z]}{z}$:
> 
> $$\frac{Y[z]}{z} = \frac{1/3}{z - 1} - \frac{5/6}{z - 0,5} + \frac{2}{z - 0,25}$$
> 
> Multiplicando por $z$ e aplicando a transformada inversa:
> 
> $$y[n] = \left[ \frac{1}{3}(1)^n - \frac{5}{6}(0,5)^n + 2(0,25)^n \right] u[n]$$
> 
> Separando as respostas temporalmente:
> 
> - **Regime Permanente ($y_{ss}[n]$):** Termo com raiz unitária que permanece para sempre:
>   $$y_{ss}[n] = \frac{1}{3}u[n]$$
> - **Transitória ($y_{tr}[n]$):** Termos que decaem para zero quando $n \to \infty$:
>   $$y_{tr}[n] = \left[ -\frac{5}{6}(0,5)^n + 2(0,25)^n \right] u[n]$$