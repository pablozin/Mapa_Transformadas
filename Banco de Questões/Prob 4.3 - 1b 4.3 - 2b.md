---
tags: [laplace, edo, entrada_nula, estado_nulo, nivel_dificil]
origem: "Lathi Prob. 4.3-1b / 4.3-2b"
---
### Problema 4.3-1 (b) & 4.3-2 (b)
Resolva a seguinte equação diferencial para $t \ge 0$:

$$\frac{d^2y}{dt^2} + 4\frac{dy}{dt} + 4y(t) = \frac{dx}{dt} + x(t)$$
Condições iniciais: $y(0^-) = 2$ e $\dot{y}(0^-) = 1$.
Entrada: $x(t) = e^{-t}u(t)$.  
Separe a resposta final em **Entrada Nula** ($y_0(t)$) e **Estado Nulo** ($y_\phi(t)$).

> [!tip]- Dica de Resolução
> Aplique Laplace mantendo os termos de condição inicial agrupados. O sistema possui raiz dupla em $s = -2$, exigindo fração do tipo $\frac{A}{(s+2)^2} + \frac{B}{s+2}$.

> [!success]- Resolução Passo a Passo
> Aplicando a transformada com condições iniciais:
> 
> $$[s^2Y(s) - 2s - 1] + 4[sY(s) - 2] + 4Y(s) = [sX(s) - 0] + X(s)$$
> 
> Agrupando os termos:
> 
> $$(s^2 + 4s + 4)Y(s) - (2s + 9) = (s + 1)X(s)$$
> 
> Como $X(s) = \frac{1}{s + 1}$, o lado direito simplifica para $(s + 1)\frac{1}{s + 1} = 1$:
> 
> $$
> (s + 2)^2 Y(s) = \underbrace{(2s + 9)}_{\text{Condições Iniciais}} + \underbrace{1}_{\text{Entrada}}
> $$
> 
> Decompondo a **Resposta de Entrada Nula ($Y_0(s)$)**:
> 
> $$Y_0(s) = \frac{2s + 9}{(s + 2)^2} = \frac{5}{(s + 2)^2} + \frac{2}{s + 2}$$
> 
> Invertendo para o tempo:
> 
> $$y_0(t) = (5te^{-2t} + 2e^{-2t})u(t)$$
> 
> Decompondo a **Resposta de Estado Nulo ($Y_\phi(s)$)**:
> 
> $$Y_\phi(s) = \frac{1}{(s + 2)^2}$$
> 
> Invertendo para o tempo:
> 
> $$y_\phi(t) = te^{-2t}u(t)$$
> 
> Somando as componentes para a resposta total:
> 
> $$y(t) = y_0(t) + y_\phi(t) = (6te^{-2t} + 2e^{-2t})u(t)$$