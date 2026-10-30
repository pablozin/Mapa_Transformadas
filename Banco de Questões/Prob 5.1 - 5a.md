---
tags:
  - transformada_z
  - inversa
  - fracoes_parciais
  - nivel_facil
origem: Lathi Prob. 5.1-5a
---
### Problema 5.1-5 (a)
Determine a transformada Z inversa unilateral de:

$$X[z] = \frac{z(z - 4)}{z^2 - 5z + 6}$$

> [!tip]- Dica de Resolução
> Regra de ouro da Transformada Z: divida a expressão por $z$ antes de calcular as frações parciais. Ao final, multiplique o $z$ de volta para usar os pares tabelados.

> [!success]- Resolução Passo a Passo
> Dividindo ambos os lados por $z$ e fatorando o denominador:
> 
> $$\frac{X[z]}{z} = \frac{z - 4}{(z - 2)(z - 3)} = \frac{A_1}{z - 2} + \frac{A_2}{z - 3}$$
> 
> Calculando os resíduos pelo método de Heaviside:
> 
> $$A_1 = \left. \frac{z - 4}{z - 3} \right|_{z = 2} = \frac{2 - 4}{2 - 3} = \frac{-2}{-1} = 2$$
> 
> $$A_2 = \left. \frac{z - 4}{z - 2} \right|_{z = 3} = \frac{3 - 4}{3 - 2} = \frac{-1}{1} = -1$$
> 
> Multiplicando o $z$ de volta em todos os termos:
> 
> $$X[z] = 2\frac{z}{z - 2} - \frac{z}{z - 3}$$
> 
> Consultando a tabela de pares imediatos (par 6: $\gamma^n u[n] \iff \frac{z}{z - \gamma}$):
> 
> $$x[n] = \left[ 2(2)^n - (3)^n \right] u[n]$$