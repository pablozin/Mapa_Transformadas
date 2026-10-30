---
tags: [transformada_z, inversa, fracoes_parciais, pegadinha, nivel_medio]
origem: "Lathi Prob. 5.1-5b"
---
### Problema 5.1-5 (b)
Determine a transformada Z inversa de:

$$X[z] = \frac{z - 4}{z^2 - 5z + 6}$$

> [!tip]- Dica de Resolução
> Cuidado: o numerador não tem o $z$ em evidência! Ao dividir por $z$, o termo vira $\frac{z - 4}{z(z - 2)(z - 3)}$. O polo na origem $\frac{k_0}{z}$ se transformará em uma constante pura quando multiplicarmos por $z$ de volta, gerando um impulso $\delta[n]$.

> [!success]- Resolução Passo a Passo
> Dividindo a expressão por $z$:
> 
> $$\frac{X[z]}{z} = \frac{z - 4}{z(z - 2)(z - 3)} = \frac{k_0}{z} + \frac{k_1}{z - 2} + \frac{k_2}{z - 3}$$
> 
> Calculando os três resíduos por Heaviside:
> 
> $$k_0 = \left. \frac{z - 4}{(z - 2)(z - 3)} \right|_{z = 0} = \frac{-4}{(-2)(-3)} = -\frac{2}{3}$$
> 
> $$k_1 = \left. \frac{z - 4}{z(z - 3)} \right|_{z = 2} = \frac{2 - 4}{2(2 - 3)} = \frac{-2}{-2} = 1$$
> 
> $$k_2 = \left. \frac{z - 4}{z(z - 2)} \right|_{z = 3} = \frac{3 - 4}{3(3 - 2)} = \frac{-1}{3} = -\frac{1}{3}$$
> 
> Multiplicando $z$ de volta em todos os membros:
> 
> $$X[z] = -\frac{2}{3} + \frac{z}{z - 2} - \frac{1}{3}\frac{z}{z - 3}$$
> 
> Invertendo termo a termo (lembrando que a constante inverte para impulso $\delta[n]$):
> 
> $$x[n] = -\frac{2}{3}\delta[n] + \left[ (2)^n - \frac{1}{3}(3)^n \right] u[n]$$