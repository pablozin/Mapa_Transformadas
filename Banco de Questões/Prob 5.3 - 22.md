---
tags: [transformada_z, funcao_transferencia, equacoes_diferenca, nivel_facil]
origem: "Lathi Prob. 5.3-22"
---
### Problema 5.3-22 (ref. 5.3-8)
Determine a função de transferência $H[z]$ para o sistema com a seguinte equação de diferenças:

$$y[n] + 2y[n - 1] + 2y[n - 2] = x[n - 1] + 2x[n - 2]$$

> [!tip]- Dica de Resolução
> Assuma o sistema em repouso. Cada atraso temporal $y[n - k]$ vira $z^{-k}Y[z]$. Ao final, multiplique o numerador e o denominador por $z^2$ para normalizar na forma de potências positivas.

> [!success]- Resolução Passo a Passo
> Aplicando a Transformada Z com condições iniciais nulas:
> 
> $$Y[z] + 2z^{-1}Y[z] + 2z^{-2}Y[z] = z^{-1}X[z] + 2z^{-2}X[z]$$
> 
> Colocando $Y[z]$ e $X[z]$ em evidência:
> 
> $$(1 + 2z^{-1} + 2z^{-2}) Y[z] = (z^{-1} + 2z^{-2}) X[z]$$
> 
> Montando a função de transferência:
> 
> $$H[z] = \frac{Y[z]}{X[z]} = \frac{z^{-1} + 2z^{-2}}{1 + 2z^{-1} + 2z^{-2}}$$
> 
> Multiplicando numerador e denominador por $z^2$ para obter a forma racional padrão:
> 
> $$H[z] = \frac{z + 2}{z^2 + 2z + 2}$$