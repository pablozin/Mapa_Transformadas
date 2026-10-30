---
tags: [laplace, realimentacao, estabilidade, diagrama_blocos, nivel_dificil]
origem: "Lathi Prob. 4.5-3b"
---
### Problema 4.5-3 (b)
Considere um sistema em malha fechada com realimentação negativa unitária cuja malha direta é dada por:

$$G(s) = \frac{K}{s(s + 2)(s + 4)}$$

Determine a faixa de valores do ganho positivo $K$ para a qual o sistema permanece BIBO estável.

> [!tip]- Dica de Resolução
> A função de transferência em malha fechada é $T(s) = \frac{G(s)}{1 + G(s)}$. Monte a tabela de Routh-Hurwitz para o denominador característico $s^3 + 6s^2 + 8s + K$ e encontre quando a primeira coluna se mantém estritamente positiva.

> [!success]- Resolução Passo a Passo
> Montando a função de transferência do sistema com realimentação:
> 
> $$T(s) = \frac{G(s)}{1 + G(s)} = \frac{K}{s(s + 2)(s + 4) + K}$$
> 
> Desenvolvendo o polinômio característico do denominador:
> 
> $$Q(s) = s(s^2 + 6s + 8) + K = s^3 + 6s^2 + 8s + K$$
> 
> Construindo a matriz do critério de Routh-Hurwitz:
> 
> $$\begin{array}{c|cc}
> s^3 & 1 & 8 \\
> s^2 & 6 & K \\
> s^1 & \frac{6 \times 8 - 1 \times K}{6} = \frac{48 - K}{6} & 0 \\
> s^0 & K & 
> \end{array}$$
> 
> Para estabilidade (todos os polos estritamente no SPE), os coeficientes da primeira coluna devem ser maiores que zero:
> 
> $$K > 0$$
> 
> $$\frac{48 - K}{6} > 0 \implies 48 - K > 0 \implies K < 48$$
> 
> Faixa de operação estável:
> 
> $$0 < K < 48$$