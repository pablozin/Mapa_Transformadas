---
tags: [laplace, propriedades, periodico, serie_geometrica, nivel_dificil]
origem: "Lathi Prob. 4.2-4a"
---
### Problema 4.2-4 (a)
Mostre que a transformada de Laplace de um sinal causal periódico $g(t)$, com período $T_0$, pode ser obtida a partir da transformada $X(s)$ de apenas o seu **primeiro período** por:

$$G(s) = \frac{X(s)}{1 - e^{-sT_0}}, \quad \text{Re}\{s\} > 0$$

> [!tip]- Dica de Resolução
> Modele o sinal periódico como uma soma de pulsos individuais defasados por múltiplos inteiros de $T_0$. Aplique a propriedade de deslocamento temporal e a soma de uma progressão geométrica infinita.

> [!success]- Resolução Passo a Passo
> Decompondo o sinal periódico causal como repetições do primeiro ciclo:
> 
> $$g(t) = x(t) + x(t - T_0) + x(t - 2T_0) + x(t - 3T_0) + \dots$$
> 
> Aplicando a transformada de Laplace termo a termo com a propriedade de atraso:
> 
> $$G(s) = X(s) + X(s)e^{-sT_0} + X(s)e^{-2sT_0} + X(s)e^{-3sT_0} + \dots$$
> 
> Colocando a transformada $X(s)$ em evidência:
> 
> $$G(s) = X(s) \left[ 1 + e^{-sT_0} + (e^{-sT_0})^2 + (e^{-sT_0})^3 + \dots \right]$$
> 
> O termo entre colchetes é uma série geométrica com razão $r = e^{-sT_0}$. Para $\text{Re}\{s\} > 0$, $|r| < 1$, permitindo aplicar a soma infinita:
> 
> $$\sum_{n=0}^{\infty} r^n = \frac{1}{1 - r} = \frac{1}{1 - e^{-sT_0}}$$
> 
> Conclui-se diretamente:
> 
> $$G(s) = \frac{X(s)}{1 - e^{-sT_0}}$$